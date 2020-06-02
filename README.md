




<p align="center"><img src="/images/logo.png" alt=""></p>
<h1 align="center">Какого Чёрта, Python! 😱</h1>
<p align="center">Изучаем и понимаем Python с помощью удивительных примеров.</p>

Переводы: [Английский English](https://github.com/satwikkansal/wtfpython) | [Китайский 中文](https://github.com/leisurelicht/wtfpython-cn) | [Добавить перевод](https://github.com/satwikkansal/wtfpython/issues/new?title=Add%20translation%20for%20[LANGUAGE]&body=Expected%20time%20to%20finish:%20[X]%20weeks.%20I%27ll%20start%20working%20on%20it%20from%20[Y].)

Другие режимы: [Интерактивный](https://colab.research.google.com/github/satwikkansal/wtfpython/blob/master/irrelevant/wtf.ipynb) | [Консольный](https://pypi.python.org/pypi/wtfpython)

Python - это прекрасный интерпретируемый высокоуровневый язык программирования, который предоставляет нам множество функций для нашего удобства. Но иногда результаты работы кода на Python могут показаться неочевидными.

Этот репозиторий - забавный проект, пытающийся объяснить, что именно происходит под капотом у некоторых неочевидных фрагментов и малоизвестных функций в Python.

Хотя некоторые из примеров, представленных ниже, могут казаться вполне логичными, но они призваны показать некоторые интересные части Python, о которых вы могли не знать. Я считаю, что это хороший способ изучить внутреннее устройство языка, и я верю, что вам это тоже будет интересно!

Если вы опытный программист на Python, вы можете принять это как вызов, и попытаться правильно понять, что делает большинство из фрагментов кода с первой попытки. Возможно, вы уже сталкивались с некоторыми из них раньше, надеюсь у меня получится освежить ваши старые сладкие воспоминания! :sweat_smile:

PS: О новых изменениях в проекте можно узнать [здесь](https://github.com/satwikkansal/wtfpython/releases/).

Итак, поехали...

# Содержание


- [Структура примеров](#структура-примеров)
    + [▶ Какое-то причудливое название](#▶-какое-то-причудливое-название)
- [Использование](#использование)
- [👀 Примеры](#👀-примеры)
  * [Секция: Напряги мозги!](#section-strain-your-brain)
    + [▶ Перво-наперво! *](#-first-things-first-)
    + [▶ Иногда строки могут быть хитрыми](#-strings-can-be-tricky-sometimes)
    + [▶ Осторожнее с цепочками операций](#-be-careful-with-chained-operations)
    + [▶ Как не надо использовать оператор `is`](#-how-not-to-use-is-operator)
    + [▶ Мистика хэширования](#-hash-brownies)
    + [▶ Deep down, we're all the same.](#-deep-down-were-all-the-same)
    + [▶ Disorder within order *](#-disorder-within-order-)
    + [▶ Keep trying... *](#-keep-trying-)
    + [▶ For what?](#-for-what)
    + [▶ Evaluation time discrepancy](#-evaluation-time-discrepancy)
    + [▶ `is not ...` is not `is (not ...)`](#-is-not--is-not-is-not-)
    + [▶ A tic-tac-toe where X wins in the first attempt!](#-a-tic-tac-toe-where-x-wins-in-the-first-attempt)
    + [▶ The sticky output function](#-the-sticky-output-function)
    + [▶ The chicken-egg problem *](#-the-chicken-egg-problem-)
    + [▶ Subclass relationships](#-subclass-relationships)
    + [▶ All-true-ation *](#-all-true-ation-)
    + [▶ The surprising comma](#-the-surprising-comma)
    + [▶ Strings and the backslashes](#-strings-and-the-backslashes)
    + [▶ not knot!](#-not-knot)
    + [▶ Half triple-quoted strings](#-half-triple-quoted-strings)
    + [▶ What's wrong with booleans?](#-whats-wrong-with-booleans)
    + [▶ Class attributes and instance attributes](#-class-attributes-and-instance-attributes)
    + [▶ Non-reflexive class method *](#-non-reflexive-class-method-)
    + [▶ yielding None](#-yielding-none)
    + [▶ Yielding from... return! *](#-yielding-from-return-)
    + [▶ Nan-reflexivity *](#-nan-reflexivity-)
    + [▶ Mutating the immutable!](#-mutating-the-immutable)
    + [▶ The disappearing variable from outer scope](#-the-disappearing-variable-from-outer-scope)
    + [▶ The mysterious key type conversion](#-the-mysterious-key-type-conversion)
    + [▶ Let's see if you can guess this?](#-lets-see-if-you-can-guess-this)
  * [Секция: Slippery Slopes](#section-slippery-slopes)
    + [▶ Modifying a dictionary while iterating over it](#-modifying-a-dictionary-while-iterating-over-it)
    + [▶ Stubborn `del` operation](#-stubborn-del-operation)
    + [▶ The out of scope variable](#-the-out-of-scope-variable)
    + [▶ Deleting a list item while iterating](#-deleting-a-list-item-while-iterating)
    + [▶ Lossy zip of iterators *](#-lossy-zip-of-iterators-)
    + [▶ Loop variables leaking out!](#-loop-variables-leaking-out)
    + [▶ Beware of default mutable arguments!](#-beware-of-default-mutable-arguments)
    + [▶ Catching the Exceptions](#-catching-the-exceptions)
    + [▶ Same operands, different story!](#-same-operands-different-story)
    + [▶ Name resolution ignoring class scope](#-name-resolution-ignoring-class-scope)
    + [▶ Needles in a Haystack *](#-needles-in-a-haystack-)
    + [▶ Splitsies *](#-splitsies-)
    + [▶ Wild imports *](#-wild-imports-)
    + [▶ All sorted? *](#-all-sorted-)
    + [▶ Midnight time doesn't exist?](#-midnight-time-doesnt-exist)
  * [Секция: The Hidden treasures!](#section-the-hidden-treasures)
    + [▶ Okay Python, Can you make me fly?](#-okay-python-can-you-make-me-fly)
    + [▶ `goto`, but why?](#-goto-but-why)
    + [▶ Brace yourself!](#-brace-yourself)
    + [▶ Let's meet Friendly Language Uncle For Life](#-lets-meet-friendly-language-uncle-for-life)
    + [▶ Even Python understands that love is complicated](#-even-python-understands-that-love-is-complicated)
    + [▶ Yes, it exists!](#-yes-it-exists)
    + [▶ Ellipsis *](#-ellipsis-)
    + [▶ Inpinity](#-inpinity)
    + [▶ Let's mangle](#-lets-mangle)
  * [Секция: Appearances are deceptive!](#section-appearances-are-deceptive)
    + [▶ Skipping lines?](#-skipping-lines)
    + [▶ Teleportation](#-teleportation)
    + [▶ Well, something is fishy...](#-well-something-is-fishy)
  * [Секция: Miscellaneous](#section-miscellaneous)
    + [▶ `+=` is faster](#--is-faster)
    + [▶ Let's make a giant string!](#-lets-make-a-giant-string)
    + [▶ Minor Ones *](#-minor-ones-)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [🎓 License](#-license)
  * [Surprise your friends as well!](#surprise-your-friends-as-well)
  * [More content like this?](#more-content-like-this)


# Структура примеров

Все примеры имеют структуру, приведённую ниже:

> ### ▶ Какое-то причудливое название
>
> ```py
> # Подготовка кода
> # Запуск "магии"...
> ```
>
> **Вывод (Версия Python`а):**
>
> ```py
> >>> triggering_statement
> Удивительный вывод команды
> ```
> (Опционально): Строка с коротким объяснением неожиданного результата
>
>
> #### 💡 Объяснение:
>
> * Краткое объяснение того, что происходит и почему.
> ```py
> # Подготовка кода
> # Дополнительные примеры для дальнейшего прояснения (при необходимости)
> ```
>  **Вывод (Версия Python`а):**
>
> ```py
> >>> trigger # Пример, который позволяет избежать неочевидной "магии"
> Ожидаемый результат
> ```

**Примечание:** Все примеры протестированы в интерактивном режиме Python 3.5.2 и они должны работать для всех версий Python`а, если это явно не указано перед выводом результатов.

# Использование

На мой взгляд, хороший способ получить максимальную отдачу от всех примеров - прочитать их в хронологическом порядке и для каждого примера:
- Внимательно читать исходный код для подготовки примера. Если вы опытный Python разработчик, вы  сможете правильно предсказать, что произойдёт в большинстве описанных случаев.
- Прочитайте фрагмент с результатом,
  + Проверьте, сходится ли он с тем, чего вы ожидали.
  + Убедитесь, что знаете конкретную причину возникновения "неожиданного" результата.
    - Если вы не знаете причину, (что вполне нормально) то сделайте глубокий вдох и прочитайте объяснение (и если вы всё ещё не понимаете, то немного покричите от злости и создайте issue [здесь](https://github.com/satwikkansal/wtfpython/issues/new)).
    - Если вы знаете причину, то нежно похлопайте себя по спине и переходите к следующему примеру. 

PS: Также можно прочитать WTFPython из консоли, используя [модуль из pypi](https://pypi.python.org/pypi/wtfpython),
```sh
$ pip install wtfpython -U
$ wtfpython
```
---

# 👀 Примеры

## Секция: Напряги мозги!

### ▶ Перво-наперво! *


По какой-то причине в Python 3.8 оператор "Walrus" (`:=`) стал довольно популярен. Давайте проверим его.

1\.

```py
# Python version 3.8+

>>> a = "wtf_walrus"
>>> a
'wtf_walrus'

>>> a := "wtf_walrus"
File "<stdin>", line 1
    a := "wtf_walrus"
      ^
SyntaxError: invalid syntax

>>> (a := "wtf_walrus") # Хотя это работает
>>> a
'wtf_walrus'
```

2 \.

```py
# Python version 3.8+

>>> a = 6, 9
>>> a
(6, 9)

>>> (a := 6, 9)
>>> a
6

>>> a, b = 6, 9 # Типичная распаковка
>>> a, b
(6, 9)
>>> (a, b = 16, 19) # Упс...
  File "<stdin>", line 1
    (a, b = 6, 9)
          ^
SyntaxError: invalid syntax

>>> (a, b := 16, 19) # А это вернёт странный кортеж из 3-х элементов
(6, 16, 19)

>>> a # Переменная 'a' всё ещё не изменилась?
6

>>> b
16
```



#### 💡 Объяснение

**Небольшая памятка про walrus оператор**

Walrus оператор (`:=`) появился в Python 3.8. Он может быть полезным в ситуациях, где вы хотите присвоить значение переменным в выражении.

```py
def some_func():
        # Предположим, что здесь происходят сложные вычисления
        # time.sleep(1000)
        return 5

# Теперь вместо,
if some_func():
        print(some_func()) # Что является плохой практикой, ведь функция вызывается дважды

# или вместо
a = some_func()
if a:
    print(a)

# Мы можем кратко написать
if a := some_func():
        print(a)
```

**Вывод (> 3.8):**

```py
5
5
5
```
Это сэкономило одну строку кода и неявно предотвратило второй вызов функции `some_func`.

- Использование walrus оператора вне скобок запрещено на внешнем уровне, поэтому возникает `SyntaxError` на строке `a := "wtf_walrus"` первого примера. Взятый в скобки код работает как ожидается и присваивает значение переменной `a`.  

- Как обычно, взятие в скобки  выражения, содержащего оператор `=`, запрещено. поэтому возникает `SyntaxError` на строке `(a, b = 6, 9)`. 

- Синтаксис walrus оператора работает по шаблону `NAME:= expr`, где `NAME` это допустимое имя, а `expr` допустимое выражение. Поэтому, упаковка и распаковка объектов не поддерживается, что значит, что, 

  - `(a := 6, 9)` является эквивалентом для `((a := 6), 9)` или `(a, 9) ` (где значение `a` равно 6)

    ```py
    >>> (a := 6, 9) == ((a := 6), 9)
    True
    >>> x = (a := 696, 9)
    >>> x
    (696, 9)
    >>> x[0] is a # Оба ссылаются на одно место в памяти
    True
    ```

  - По тому же принципу, `(a, b := 16, 19)` эквивалентно `(a, (b := 16), 19)`, что просто является кортежем из 3-х элементов. 

---

### ▶ Иногда строки могут быть хитрыми

1\.

```py
>>> a = "some_string"
>>> id(a)
140420665652016
>>> id("some" + "_" + "string") # Обратите внимание, что id одинаковые
140420665652016
```

2\.
```py
>>> a = "wtf"
>>> b = "wtf"
>>> a is b
True

>>> a = "wtf!"
>>> b = "wtf!"
>>> a is b
False

```

3\.

```py
>>> a, b = "wtf!", "wtf!"
>>> a is b # Все версии, кроме 3.7.x
True

>>> a = "wtf!"; b = "wtf!"
>>> a is b # Вернёт True или False в зависимости от мнста вызова (интерпретатор / ipython / отдельный скрипт)
False
```

```py
# В этот раз в файле some_file.py
a = "wtf!"
b = "wtf!"
print(a is b)

# Напечатает True при запуске
```

4\.

**Вывод(< Python3.7 )**

```py
>>> 'a' * 20 is 'aaaaaaaaaaaaaaaaaaaa'
True
>>> 'a' * 21 is 'aaaaaaaaaaaaaaaaaaaaa'
False
```

Имеет смысл, верно?

#### 💡 Объяснение:
+ Такое поведение в первом и втором фрагментах происходит из-за оптимизации CPython (называемой string interning), которая в некоторых случаях пытается использовать существующие неизменяемые объекты, а не каждый раз создавать новый объект.
+ После "интернирования" многие переменные могут ссылаться на один и тот же объект в памяти, тем самым экономя память.
+ В приведенных выше фрагментах строки неявно "интернированы". Решение о том, когда неявно интернировать строку, зависит от реализации. Есть несколько правил, которые можно использовать, чтобы угадать, будет ли строка интернирована или нет:
  * Все строки длины 0 и 1 интернируются.
  * Строки интернируются в compile time (`'wtf'` будет интернирована, но `''.join(['w', 't', 'f'])` не будет)
  * Строки, которые состоят не только из ASCII символов, цифр и подчёркиваний не будут интернироваться. Это объясняет, почему `'wtf!'` не была интернирована из-за символа `!`. Описание этого правила в реализации CPython может быть найдено [здесь](https://github.com/python/cpython/blob/3.6/Objects/codeobject.c#L19)
  ![image](/images/string-intern/string_intern.png)
+ Когда значение `a` и `b` устанавливаются в `"wtf!"` в одной строке, интерпретатор Python  создаёт новый объект, затем ссылает вторую переменную на созданный объект. Если делать это на разных строках, то интерпретатор не "знает", что `"wtf!"` уже существует, как объект (потому что с `"wtf!"` не происходит неявного интернирования по правилам, описанным выше). Это compile-time оптимизация. Она не применяется к версиям CPython 3.7.x (подробнее в этом [issue](https://github.com/satwikkansal/wtfpython/issues/100)).
+ Блок компиляции в интерактивном окружении (например в IPython) состоит из одиночного выражения, тогда как в случае модуля,  блок компиляции включает весь модуль. `a, b = "wtf!", "wtf!"` это одиночное выражение, тогда как `a = "wtf!"; b = "wtf!"` это два выражения в одной строке. Это объясняет, почему переменные ссылаются на разную память в случае с `a = "wtf!"; b = "wtf!"`, и также это объясняет, почему они ссылаются на одну память в случае запуска в виде модуля `some_file.py`
+ Внезапное изменение вывода четвёртого врагмента связано с  [peephole оптимизацией](https://en.wikipedia.org/wiki/Peephole_optimization), техникой, известной, как Constant folding. Это значит, что выражение `'a'*20` заменяется на `'aaaaaaaaaaaaaaaaaaaa'` на этапе компиляции, чтобы сохранить немного времени в runtime. Constant folding применяется только для строк, длина которых меньше 20. (Почему? Представьте размер `.pyc` файла, который будет сгенерирован в результате выполнения `'a'*10**10`). [Здесь](https://github.com/python/cpython/blob/3.6/Python/peephole.c#L288) можно посмотреть детали реализации.
+ Примечание: В Python 3.7, оптимизация Constant folding была перемещена из peephole оптимизатора в новый AST оптимизатор с некоторыми изменениями в логике, поэтому приведённые фрагменты не работают в Python 3.7. Об этом изменении можно узнать больше [здесь](https://bugs.python.org/issue11549). 

---


### ▶ Осторожнее с цепочками операций
```py
>>> (False == False) in [False] # имеет смысл
False
>>> False == (False in [False]) # имеет смысл
False
>>> False == False in [False] # что теперь?
True

>>> True is False == False
False
>>> False is False is False
True

>>> 1 > 0 < 1
True
>>> (1 > 0) < 1
False
>>> 1 > (0 < 1)
False
```

#### 💡 Объяснение:

Согласно https://docs.python.org/2/reference/expressions.html#not-in

> Formally, if a, b, c, ..., y, z are expressions and op1, op2, ..., opN are comparison operators, then a op1 b op2 c ... y opN z is equivalent to a op1 b and b op2 c and ... y opN z, except that each expression is evaluated at most once.

Хотя приведённые выше примеры могут показаться глупыми примерах, но цепочки операций работают фантастически с такими вещами, как `a == b == c` и `0 <= x <= 100`.

* `False is False is False` эквивалентно `(False is False) and (False is False)`
* `True is False == False` эквивалентно `True is False and False == False` и поскольку первая часть выражения (`True is False`) равна `False`, то всё выражение вычисляется в `False`.
* `1 > 0 < 1` эквивалентно `1 > 0 and 0 < 1`, а это вычисляется в `True`.
* Выражение `(1 > 0) < 1` эквивалентно `True < 1` and
  ```py
  >>> int(True)
  1
  >>> True + 1 # не относится сюда, но довольно весело
  2
  ```
  Поэтому, `1 < 1` вычисляутся в `False`

---

### ▶ Как не надо использовать оператор `is`
Ниже приведён очень известный пример, который часто встречается в интернете.

1\.

```py
>>> a = 256
>>> b = 256
>>> a is b
True

>>> a = 257
>>> b = 257
>>> a is b
False
```

2\.

```py
>>> a = []
>>> b = []
>>> a is b
False

>>> a = tuple()
>>> b = tuple()
>>> a is b
True
```

3\.
**Вывод**

```py
>>> a, b = 257, 257
>>> a is b
True
```

**Вывод (Python 3.7.x)**

```py
>>> a, b = 257, 257
>> a is b
False
```

#### 💡 Объяснение:

**Разница между `is` и `==`**

* Оператор `is` проверяет, что операнды ссылаются на один и тот же объект (то есть он проверяет, совпадает ли "идентичность" операндов или нет).
* Оператор `==` сравнивает значения обоих операндов и проверяет, равны ли они.
* Получается, что `is` применяется для проверки ссылочного равенство, а `==` для проверки равенства по значению. Пример, чтобы прояснить ситуацию,
  ```py
  >>> class A: pass
  >>> A() is A() # Здесь два пустых объекта в РАЗНЫХ местах памяти.
  False
  ```

**`256` это существующий объект, а `257` - нет**

Когда Python запускается, числа от `-5` до `256` выделяются в памяти. Эти числа используются очень часто, поэтому имеет смысл заранее подготовить их.

Подробнее в документации https://docs.python.org/3/c-api/long.html
> The current implementation keeps an array of integer objects for all integers between -5 and 256, when you create an int in that range you just get back a reference to the existing object. So it should be possible to change the value of 1. I suspect the behavior of Python, in this case, is undefined. :-)

```py
>>> id(256)
10922528
>>> a = 256
>>> b = 256
>>> id(a)
10922528
>>> id(b)
10922528
>>> id(257)
140084850247312
>>> x = 257
>>> y = 257
>>> id(x)
140084850247440
>>> id(y)
140084850247344
```

В данном случае интерпретатор недостаточно умён, чтобы распознать, что во время `y = 257` он уже создал число со значением `257`, поэтому он создаёт ещё один объект в памяти.

Схожие оптимизации применяются для **неизменяемых** объектов, вроде пустых кортежей. Так как списки являются изменяемыми `[] is []` вернёт `False`, а `() is ()` вернёт `True`. Это объясняет второй пример. Перейдём к третьему, 

**Обе переменные `a` и `b` ссылаются на один и тот же объект, когда инициализируются одним значением на одной и той же строке.**

**Вывод:**

```py
>>> a, b = 257, 257
>>> id(a)
140640774013296
>>> id(b)
140640774013296
>>> a = 257
>>> b = 257
>>> id(a)
140640774013392
>>> id(b)
140640774013488
```

* Когда `a` и `b` устанавливаются равными `257` на одной строке, интерпретатор Python создает новый объект, а затем обе переменных ссылаются на него одновременно. Если вы делаете инициализацию в отдельных строках, то интерпретатор не «знает», что уже есть «257» как объект.

* Это оптимизация компилятора, которая в особенности относится к интерактивной среде. Когда вы вводите две строки в интерпретаторе, они компилируются отдельно, поэтому и оптимизируются отдельно. Если бы вы попробовали запустить этот пример в файле `.py`, вы бы не увидели такое же поведение, потому что файл компилируется полностью. Эта оптимизация не ограничивается целыми числами, она работает для других неизменяемых типов данных, таких как кортежи, строки и числа с плавающей точкой,
  ```py
  >>> a, b = 257.0, 257.0
  >>> a is b
  True
  ```

* Почему это не работает в Python 3.7? Причина в том что оптимизации компиляции зависят от реализации и могут меняться с версиями Python или разными ОС. Я всё ещё разбираюсь, какое конкретно изменение в Python 3.7 привело к изменению поведения. Подробнее с этим можно познакомиться в этом [issue](https://github.com/satwikkansal/wtfpython/issues/100).

---


### ▶ Мистика хэширования
1\.
```py
some_dict = {}
some_dict[5.5] = "JavaScript"
some_dict[5.0] = "Ruby"
some_dict[5] = "Python"
```

**Вывод:**

```py
>>> some_dict[5.5]
"JavaScript"
>>> some_dict[5.0] # "Python" уничтожает "Ruby"?
"Python"
>>> some_dict[5] 
"Python"

>>> complex_five = 5 + 0j
>>> type(complex_five)
complex
>>> some_dict[complex_five]
"Python"
```

Почему же Python повсюду?


#### 💡 Объяснение:

* Уникальность ключей в словаре Python является *эквивалентностью* (`==`), а не идентичностью (`is`). Таким образом, хотя `5`,` 5.0` и `5 + 0j` являются различными объектами разных типов, поскольку они равны (эквивалентны), они не могут быть в одном и том же` dict` (или `set`). Как только вы вставите любой из них, попытка найти любой другой с тем же значением, но другим типом будет успешной и вернёт исходное значение, а не `KeyError`:
  ```py
  >>> 5 == 5.0 == 5 + 0j
  True
  >>> 5 is not 5.0 is not 5 + 0j
  True
  >>> some_dict = {}
  >>> some_dict[5.0] = "Ruby"
  >>> 5.0 in some_dict
  True
  >>> (5 in some_dict) and (5 + 0j in some_dict)
  True
  ```
  * Это относится и к назначению элемента. Поэтому, когда вы пишете `some_dict[5] =" Python "`, Python находит существующий элемент с эквивалентным ключом `5.0 ->" Ruby "`, и перезаписывает его значение, отбрасывая новый ключ (`5`).
  ```py
  >>> some_dict
  {5.0: 'Ruby'}
  >>> some_dict[5] = "Python"
  >>> some_dict
  {5.0: 'Python'}
  ```
* Так как же мы можем обновить ключ и сделать его равным `5` (вместо` 5.0`)? На самом деле мы не можем сделать этого за раз, но мы можем сначала удалить ключ (`del some_dict [5.0]`), а затем установить новый (`some_dict [5]`), чтобы получить целое число `5` в качестве ключа вместо плавающего `5.0`, хотя это бывает необходимо в редких случаях.

* Как Python нашел `5` в словаре, содержащем `5.0`? Python делает это за константное время, не просматривая каждый ключ словаря. Когда Python ищет ключ `5` в словаре, он сначала вычисляет `hash(5)`, после чего ищет ключ с таким же хэшем  ([подробнее здесь](https://docs.python.org/3/reference/datamodel.html#object.__hash__)), а у чисел `5` , `5.0` и` 5 + 0j`  значение хеш-функции одинаковое.
  ```py
  >>> 5 == 5.0 == 5 + 0j
  True
  >>> hash(5) == hash(5.0) == hash(5 + 0j)
  True
  ```
  **Примечание:**  Объекты с одинаковым хэшем могут не быть одинаковыми. (Это явление известно под названием [коллиция хэш функции](https://en.wikipedia.org/wiki/Collision_(computer_science)), и она ухудшает производительность алгоритмов, использующих хэширование)

---

### ▶ В глубине души мы все одинаковые
```py
class WTF:
  pass
```

**Вывод:**
```py
>>> WTF() == WTF() # два разных объекта не могут быть равны
False
>>> WTF() is WTF() # объект не является таким же объектом
False
>>> hash(WTF()) == hash(WTF()) # хэши также _должны_ быть разными
True
>>> id(WTF()) == id(WTF())
True
```

#### 💡 Объяснение:

* Когда вызывается `id`, Python создаёт объект класса `WTF` и передаёт его в функцию `id`. Функция `id` принимает `id` объекта (адрес в памяти), и выбрасывает объект. Он уничтожается.
* Когда мы делаем это два раза подряд, Python выделяет общую память для объектов. Так как в CPython функция `id` использует адрес в памяти в качестве id объекта, то id двух объектов совпадают.
* Поэтому, id объекта уникально только во время существования этого объекта. После того, как объект уничтожен, или перед тем, как объект создан, что-то ещё может иметь тот же id.
* Но почему оператор `is` вернул `False`? Давайте взглянем снова.
  ```py
  class WTF(object):
    def __init__(self): print("I")
    def __del__(self): print("D")
  ```

  **Вывод:**
  ```py
  >>> WTF() is WTF()
  I
  I
  D
  D
  False
  >>> id(WTF()) == id(WTF())
  I
  D
  I
  D
  True
  ```
  Как вы можете заметить, порядок, в котором объекты уничтожаются, является причиной необычных результатов.

---

### ▶ Беспорядок в порядке *
```py
from collections import OrderedDict

dictionary = dict()
dictionary[1] = 'a'; dictionary[2] = 'b';

ordered_dict = OrderedDict()
ordered_dict[1] = 'a'; ordered_dict[2] = 'b';

another_ordered_dict = OrderedDict()
another_ordered_dict[2] = 'b'; another_ordered_dict[1] = 'a';

class DictWithHash(dict):
    """
    A dict that also implements __hash__ magic.
    """
    __hash__ = lambda self: 0

class OrderedDictWithHash(OrderedDict):
    """
    An OrderedDict that also implements __hash__ magic.
    """
    __hash__ = lambda self: 0
```

**Вывод**
```py
>>> dictionary == ordered_dict # Если a == b
True
>>> dictionary == another_ordered_dict # и b == c
True
>>> ordered_dict == another_ordered_dict # тогда и c == a ??
False

# Все мы знаем, что set содержит только уникальные элементы,
# давайте попробуем создать set словаря и посмотреть, что случится...

>>> len({dictionary, ordered_dict, another_ordered_dict})
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unhashable type: 'dict'

# Имеет смысл, ведь словарь не содержит реализации __hash__, давайте используем
# наши классы обёртки.
>>> dictionary = DictWithHash()
>>> dictionary[1] = 'a'; dictionary[2] = 'b';
>>> ordered_dict = OrderedDictWithHash()
>>> ordered_dict[1] = 'a'; ordered_dict[2] = 'b';
>>> another_ordered_dict = OrderedDictWithHash()
>>> another_ordered_dict[2] = 'b'; another_ordered_dict[1] = 'a';
>>> len({dictionary, ordered_dict, another_ordered_dict})
1
>>> len({ordered_dict, another_ordered_dict, dictionary}) # изменяем порядок переменных
2
```

Что здесь происходит?

#### 💡 Объяснение:

- Причиной, по которой появляется разный результат, в зависимости от порядка `dictionary`, `ordered_dict` и `another_ordered_dict` заключается в способе реализации метода `__eq__` в классе `OrderedDict`. Цитата из [документации](https://docs.python.org/3/library/collections.html#ordereddict-objects)
  
    > Equality tests between OrderedDict objects are order-sensitive and are implemented as `list(od1.items())==list(od2.items())`. Equality tests between `OrderedDict` objects and other Mapping objects are order-insensitive like regular dictionaries.
- Такая реализация проверки на равенство позволяет подставлять объект класса `OrderedDict` в любое место, где используется обычный словарь.
- Хорошо, так почему же изменение порядка переменных повлияло на длину получивщегося объекта `set`? Ответ в недостатке непереходности равенства. Так как множества это "неупорядоченная" коллекция уникальных элементов, порядок, в котором элементы добавляются, не должен влиять, но в нашем случае он влияет. Давайте разберёмся,
    ```py
    >>> some_set = set()
    >>> some_set.add(dictionary) # это объект из примера выше
    >>> ordered_dict in some_set
    True
    >>> some_set.add(ordered_dict)
    >>> len(some_set)
    1
    >>> another_ordered_dict in some_set
    True
    >>> some_set.add(another_ordered_dict)
    >>> len(some_set)
    1

    >>> another_set = set()
    >>> another_set.add(ordered_dict)
    >>> another_ordered_dict in another_set
    False
    >>> another_set.add(another_ordered_dict)
    >>> len(another_set)
    2
    >>> dictionary in another_set
    True
    >>> another_set.add(another_ordered_dict)
    >>> len(another_set)
    2
    ```
    Строка `another_ordered_dict in another_set` возвращает `False`, так как в `another_set` присутствует `order_dict`, а `order_dict == another_ordered_dict` равно `False`.

---

### ▶ Продолжай пытаться... *
```py
def some_func():
    try:
        return 'from_try'
    finally:
        return 'from_finally'

def another_func(): 
    for _ in range(3):
        try:
            continue
        finally:
            print("Finally!")

def one_more_func(): # Попался!
    try:
        for i in range(3):
            try:
                1 / i
            except ZeroDivisionError:
                # Попробуем бросить исключение здесь и поймать его вне цикла
                raise ZeroDivisionError("A trivial divide by zero error")
            finally:
                print("Iteration", i)
                break
    except ZeroDivisionError as e:
        print("Zero division error occurred", e)
```

**Вывод:**

```py
>>> some_func()
'from_finally'

>>> another_func()
Finally!
Finally!
Finally!

>>> 1 / 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero

>>> one_more_func()
Iteration 0

```

#### 💡 Объяснение:

- Когда `return`, `break` или `continue` выполняются внутри блока `try`, принадлежащего выражению "try…finally", тогда при выходе из блока try также выполняется блок `finally`.
- Возвращаемое значение функции определяется последним выполненным выражением `return`. Так как блок `finally` всегда исполняется, то выражение `return`, записанное в блоке `finally` всегда будет выполнено последним.
- Хитрость в том, что если блок finally содержит команду `return` или `break`, то проброс нового временного исключения не обрабатывается.

---


### ▶ For what?
```py
some_string = "wtf"
some_dict = {}
for i, some_dict[i] in enumerate(some_string):
    i = 10
```

**Вывод:**
```py
>>> some_dict # Словарь заполнился индексами и символами.
{0: 'w', 1: 't', 2: 'f'}
```

####  💡 Объяснение:

* Выражение `for` определено в [грамматике Python](https://docs.python.org/3/reference/grammar.html) как:
  ```
  for_stmt: 'for' exprlist 'in' testlist ':' suite ['else' ':' suite]
  ```
  Где `exprlist` это цель присваивания. Это значит, что **для каждого элемента выполняется**   `{exprlist} = {next_value}`.
  Интересный пример для иллюстрации:
  ```py
  for i in range(4):
      print(i)
      i = 10
  ```

  **Вывод:**
  ```
  0
  1
  2
  3
  ```

  Вы думали, что цикл сработает один раз?

  **💡 Объяснение:**

  - Выражение присваивания `i = 10` никогда не воздействует на иттерацию цикла, из-за способа работы цикла for в Python. Перед началом каждой иттерации, следующий объект из иттератора (в нашем случае `range(4)`) распаковывается и присваивается списку переменных цикла (в нашем случае `i`).

* Функция `enumerate(some_string)` генерирует новое значение для `i` (возрастающий счётчик) для каждого символа из `some_string`. После этого,  ключ `i` у словаря `some_dict` присваивается символу строки. Все шаги цикла выглядят так:
  ```py
  >>> i, some_dict[i] = (0, 'w')
  >>> i, some_dict[i] = (1, 't')
  >>> i, some_dict[i] = (2, 'f')
  >>> some_dict
  ```

---

### ▶ Evaluation time discrepancy
1\.
```py
array = [1, 8, 15]
# Типичный генератор
gen = (x for x in array if array.count(x) > 0)
array = [2, 8, 22]
```

**Вывод:**

```py
>>> print(list(gen)) # Куда делись остальные значения?
[8]
```

2\.

```py
array_1 = [1,2,3,4]
gen_1 = (x for x in array_1)
array_1 = [1,2,3,4,5]

array_2 = [1,2,3,4]
gen_2 = (x for x in array_2)
array_2[:] = [1,2,3,4,5]
```

**Вывод:**
```py
>>> print(list(gen_1))
[1, 2, 3, 4]

>>> print(list(gen_2))
[1, 2, 3, 4, 5]
```

3\.

```py
array_3 = [1, 2, 3]
array_4 = [10, 20, 30]
gen = (i + j for i in array_3 for j in array_4)

array_3 = [4, 5, 6]
array_4 = [400, 500, 600]
```

**Вывод:**
```py
>>> print(list(gen))
[401, 501, 601, 402, 502, 602, 403, 503, 603]
```

#### 💡 Объяснение:

- In a [generator](https://wiki.python.org/moin/Generators) expression, the `in` clause is evaluated at declaration time, but the conditional clause is evaluated at runtime.
- So before runtime, `array` is re-assigned to the list `[2, 8, 22]`, and since out of `1`, `8` and `15`, only the count of `8` is greater than `0`, the generator only yields `8`.
- The differences in the output of `g1` and `g2` in the second part is due the way variables `array_1` and `array_2` are re-assigned values.
- In the first case, `array_1` is binded to the new object `[1,2,3,4,5]` and since the `in` clause is evaluated at the declaration time it still refers to the old object `[1,2,3,4]` (which is not destroyed).
- In the second case, the slice assignment to `array_2` updates the same old object `[1,2,3,4]` to `[1,2,3,4,5]`. Hence both the `g2` and `array_2` still have reference to the same object (which has now been updated to `[1,2,3,4,5]`).
- Okay, going by the logic discussed so far, shouldn't be the value of `list(g)` in the third snippet be `[11, 21, 31, 12, 22, 32, 13, 23, 33]`? (because `array_3` and `array_4` are going to behave just like `array_1`). The reason why (only) `array_4` values got updated is объясняется в [PEP-289](https://www.python.org/dev/peps/pep-0289/#the-details)
  
    > Only the outermost for-expression is evaluated immediately, the other expressions are deferred until the generator is run.

---


### ▶ `is not ...` это не `is (not ...)`
```py
>>> 'something' is not None
True
>>> 'something' is (not None)
False
```

#### 💡 Объяснение:

- `is not` это один бинарный оператор и его поведение отличается от `is` и `not` по-отдельности.
- `is not` вычисляется в `False` если переменные по обе стороны от оператора указывают на один объект в памяти и `True` в остальных случаях. 
- В нашем примере, `(not None)` вычисляется в `True`, поскольку `None` в булевом контексте приводится к `False`, поэтому всё выражение превращается в `'something' is True`.

---

### ▶ Крестики-нолики, где Х выигрывает с первой попытки!

```py
# Инициализируем ряд двумерной доски
row = [""] * 3 # ряд i['', '', '']
# Создадим доску
board = [row] * 3
```

**Вывод:**

```py
>>> board
[['', '', ''], ['', '', ''], ['', '', '']]
>>> board[0]
['', '', '']
>>> board[0][0]
''
>>> board[0][0] = "X"
>>> board
[['X', '', ''], ['X', '', ''], ['X', '', '']]
```

Мы ведь присвоили только `"X"` один раз, разве нет?

#### 💡 Объяснение:

Когда мы инициализируем переменную `row`, в памяти происходит следующее:

![image](/images/tic-tac-toe/after_row_initialized.png)

И когда переменная `board` инициализируется умножением `row` на число, то внутри памяти происходит следующее: (Элементы `board[0]`, `board[1]` и `board[2]` ссылаются на один и тот же лист `row`)

![image](/images/tic-tac-toe/after_board_initialized.png)

Мы можем избежать этого, не используя переменную `row` для генерации `board`. (Подробнее в [этом issue](https://github.com/satwikkansal/wtfpython/issues/68)).

```py
>>> board = [['']*3 for _ in range(3)]
>>> board[0][0] = "X"
>>> board
[['X', '', ''], ['', '', ''], ['', '', '']]
```

---

### ▶ Липкий вывод

1\.

```py
funcs = []
results = []
for x in range(7):
    def some_func():
        return x
    funcs.append(some_func)
    results.append(some_func())  # Обратите внимание на вызов функции

funcs_results = [func() for func in funcs]
```

**Вывод:**

```py
>>> results
[0, 1, 2, 3, 4, 5, 6]
>>> funcs_results
[6, 6, 6, 6, 6, 6, 6]
```
Несмотря на то, что значения `x` были различными на каждом шаге цикла, но из-да добавления `some_func` в список `funcs`, все функции списка вернули 6.

2\.

```py
>>> powers_of_x = [lambda x: x**i for i in range(10)]
>>> [f(2) for f in powers_of_x]
[512, 512, 512, 512, 512, 512, 512, 512, 512, 512]
```

#### 💡 Объяснение:
- При определении функции, которая использует переменную цикла внутри цикла, замыкание функции  привязывается к переменной, а не к ее значению. Таким образом, все функции используют последнее значение переменной для вычисления значения функции.

- Чтобы получить желаемое поведение, вы можете передать переменную цикла как **именованную** переменную функции. **Но почему это сработает?** Потому что это определит переменную в области видимости функции.

    ```py
    funcs = []
    for x in range(7):
        def some_func(x=x):
            return x
        funcs.append(some_func)
    ```

    **Вывод:**
    ```py
    >>> funcs_results = [func() for func in funcs]
    >>> funcs_results
    [0, 1, 2, 3, 4, 5, 6]
    ```

---

### ▶ Проблема курицы и яйца *
1\.
```py
>>> isinstance(3, int)
True
>>> isinstance(type, object)
True
>>> isinstance(object, type)
True
```

Так что же является "универсальным" базовым классом? Давайте добавим ещё больше путанницы.

2\. 

```py
>>> class A: pass
>>> isinstance(A, A)
False
>>> isinstance(type, type)
True
>>> isinstance(object, object)
True
```

3\.

```py
>>> issubclass(int, object)
True
>>> issubclass(type, object)
True
>>> issubclass(object, type)
False
```


#### 💡 Объяснение:

- `type` является [метаклассом](https://realpython.com/python-metaclasses/) в Python.
- **Всё** является классом `object` в Python, включая классы и их объекты (инстансы).
- Класс `type` является метаклассом класса `object` и каждый класс (включая `type`) наследуются от `object`.
- У классов `object` и `type` нет базового класса. Путанница в примере выше возникает из-за того, что мы размышляем про отношения классов (`issubclass` и `isinstance`) в терминах Python. Взаимоотношения классов `object` и `type` не могут быть воспроизведены в чистом Python. Эти отношения выглядят так:
    + Класс A является экземпляром класса B, а класс B является экземпляром класса A.
    + Класс A является экземпляром самого себя.
- Такие отношения между `object` и `type` (оба являются экземплярами себя и друг-друга) существуют в Python только из-за "хитростей" на уровне реализации и не могут быть воспроизведены.

---

### ▶ Отношение подкласса
**Вывод:**
```py
>>> from collections import Hashable
>>> issubclass(list, object)
True
>>> issubclass(object, Hashable)
True
>>> issubclass(list, Hashable)
False
```

Отношения между подклассами должны быть транзитивными, ведь так? (Если `A` подкласс `B`, и `B` это подкласс  `C`, тогда `A` _должно_ быть подклассом `C`)

#### 💡 Объяснение:

* Отношения между подклассами не обязательно являются транзитивными в Python. Любой может определить свой метод `__subclasscheck__` в метаклассе.
* Когда вызывается `issubclass(cls, Hashable)`, функция ищет  "`__hash__`" метод у `cls` или у классов-родителей.
* Поскольку `object` хэшируемы, но `list` нет, это "ломает" транзитивность отношения.
* Более детальное объяснение можно найти [здесь](https://www.naftaliharris.com/blog/python-subclass-intransitivity/).

---

### ▶ Вся правда *


```py
>>> all([True, True, True])
True
>>> all([True, True, False])
False

>>> all([])
True
>>> all([[]])
False
>>> all([[[]]])
True
```

Почему же "Правда" сменяется "Ложью"?

#### 💡 Объяснение:

- Реализация функции `all` эквивалентна коду:
```py
  def all(iterable):
      for element in iterable:
          if not element:
              return False
      return True
  ```

- `all([])` вернёт`True`, так как `iterable` пустой. 
- `all([[]])` вернёт `False` , так как `not []` это `True`, ведь оно эквивалентно `not False`, поскольку список внутри `iterable` пуст.
- `all([[[]]])` и последующие вложенные варианты всегда дадут `True`, поскольку `not [[]]`, `not [[[]]]`, и т.д. эквивалентны `not True`.

---

### ▶ Внезапная запятая
**Вывод (< 3.6):**

```py
>>> def f(x, y,):
...     print(x, y)
...
>>> def g(x=4, y=5,):
...     print(x, y)
...
>>> def h(x, **kwargs,):
  File "<stdin>", line 1
    def h(x, **kwargs,):
                     ^
SyntaxError: invalid syntax

>>> def h(*args,):
  File "<stdin>", line 1
    def h(*args,):
                ^
SyntaxError: invalid syntax
```

#### 💡 Объяснение:

- Висячая запятая не всегда допустима в списке аргументов функции.
-  В Python, список аргументов частично определяется начальными запятыми и частично конечными. Иногда это может создать конфликт, в котором запятая находится "в ловушке" и не подходит не под одно правило синтаксиса.
-  **Примечание:** Проблема с запятой [решена в Python 3.6](https://bugs.python.org/issue9232). Заметка [здесь](https://bugs.python.org/issue9232#msg248399) рассказывает о разных применениях запятой в Python.

---

### ▶ Строки и бекслэши
**Вывод:**
```py
>>> print("\"")
"

>>> print(r"\"")
\"

>>> print(r"\")
File "<stdin>", line 1
    print(r"\")
              ^
SyntaxError: EOL while scanning string literal

>>> r'\'' == "\\'"
True
```

#### 💡 Объяснение:

- В обычной строке, бекслэш используется, чтобы экранировать символ, который может иметь специальное значение (например, кавычки, бекслэш и др.).
    ```py
    >>> "wt\"f"
    'wt"f'
    ```
- В сырых строках (с префиксом `r`),  бекслэш не экранирует символы.
    ```py
    >>> r'wt\"f' == 'wt\\"f'
    True
    >>> print(repr(r'wt\"f')
    'wt\\"f'

    >>> print("\n")

    >>> print(r"\\n")
    '\\\\n'
    ```
- Это означает, что когда парсер встречает бекслэш в строке (даже в сырой), он ожидает ещё один символ, следующий за ним. А в нашем случае (`print(r"\")`), бекслэш экранирует кавычку, оставляя парсер без  закрывающей кавычки (из-за этого получаем `SyntaxError`). Поэтому бекслэши не работают на конце сырой строки.

---

### ▶ не узел!
```py
x = True
y = False
```

**Вывод:**
```py
>>> not x == y
True
>>> x == not y
  File "<input>", line 1
    x == not y
           ^
SyntaxError: invalid syntax
```

#### 💡 Объяснение:

* Приоритет операторов влияет на то, как выражение будет вычисляться, а оператор `==` имеет больший приоритет, чем оператор `not`.
* Поэтому `not x == y` эквивалентно `not (x == y)`, что эквивалентно `not (True == False)`, которое вычисляется в `True`.
* Но `x == not y` вызывает `SyntaxError` потому что оно интерпретируется как `(x == not) y`, а не как `x == (not y)`.
* Парсер ожидает, что токен `not` будет частью оператора `not in` (так как  `==` и `not in` имеют одинаковый приоритет), но после того, как парсер не находит токен `in` следующий за токеном `not`, он выбрасывает `SyntaxError`.

---

### ▶ Половина строки в тройных кавычках
**Вывод:**
```py
>>> print('wtfpython''')
wtfpython
>>> print("wtfpython""")
wtfpython
>>> # Следующая строчка выбросит `SyntaxError`
>>> # print('''wtfpython')
>>> # print("""wtfpython")
  File "<input>", line 3
    print("""wtfpython")
                        ^
SyntaxError: EOF while scanning triple-quoted string literal
```

#### 💡 Объяснение:
+ Python поддерживает неявную[конкатенацию строковых литералов](https://docs.python.org/2/reference/lexical_analysis.html#string-literal-concatenation), Example,
  ```
  >>> print("wtf" "python")
  wtfpython
  >>> print("wtf" "") # or "wtf"""
  wtf
  ```
+ `'''` и `"""` в первом случае интерпретируются, как склейка исходной строки с пустой. А в случае с  ошибкой возникает `SyntaxError` из-за того, что интерпретатор ожидает завершающую тройную кавычку, так как он уже встретил открывающую.

---

### ▶ Что не так с логикой?
1\.

```py
# Простой пример для подсчёта булевых и целых
# в списке со смешанными типами данных.
mixed_list = [False, 1.0, "some_string", 3, True, [], False]
integers_found_so_far = 0
booleans_found_so_far = 0

for item in mixed_list:
    if isinstance(item, int):
        integers_found_so_far += 1
    elif isinstance(item, bool):
        booleans_found_so_far += 1
```

**Вывод:**
```py
>>> integers_found_so_far
4
>>> booleans_found_so_far
0
```


2\.
```py
>>> some_bool = True
>>> "wtf" * some_bool
'wtf'
>>> some_bool = False
>>> "wtf" * some_bool
''
```

3\.

```py
def tell_truth():
    True = False
    if True == False:
        print("I have lost faith in truth!")
```

**Вывод (< 3.x):**

```py
>>> tell_truth()
I have lost faith in truth!
```



#### 💡 Объяснение:

* `bool` это подкласс `int` в Python
    
    ```py
    >>> issubclass(bool, int)
    True
    >>> issubclass(int, bool)
    False
    ```
    
* Поэтому `True` и `False` являются экземплярами `int`
  ```py
  >>> isinstance(True, int)
  True
  >>> isinstance(False, int)
  True
  ```

* Значение `True` равно `1`, а значение `False` равно `0`.
  ```py
  >>> int(True)
  1
  >>> int(False)
  0
  ```

* Подробнее на StackOverflow [в этом ответе](https://stackoverflow.com/a/8169049/4354153).

* Изначально в Python не было типа `bool` (люди использовали 0 для false и любое другое число для true).  Значения `True`, `False`, и тип `bool` были добавлены в версии 2.x, но для обратной совместимости, `True` и `False` были сделаны целыми и их даже можно было изменить их значение. 

* Python 3 сломал обратную совместимость, что позволило решить эту проблему, из-за чего последний пример не заработает в  версии Python 3.x!

---

### ▶ Аттрибуты класса и экземпляра
1\.
```py
class A:
    x = 1

class B(A):
    pass

class C(A):
    pass
```

**Вывод:**
```py
>>> A.x, B.x, C.x
(1, 1, 1)
>>> B.x = 2
>>> A.x, B.x, C.x
(1, 2, 1)
>>> A.x = 3
>>> A.x, B.x, C.x # C.x изменился, но B.x нет
(3, 2, 3)
>>> a = A()
>>> a.x, A.x
(3, 3)
>>> a.x += 1
>>> a.x, A.x
(4, 3)
```

2\.
```py
class SomeClass:
    some_var = 15
    some_list = [5]
    another_list = [5]
    def __init__(self, x):
        self.some_var = x + 1
        self.some_list = self.some_list + [x]
        self.another_list += [x]
```

**Вывод:**

```py
>>> some_obj = SomeClass(420)
>>> some_obj.some_list
[5, 420]
>>> some_obj.another_list
[5, 420]
>>> another_obj = SomeClass(111)
>>> another_obj.some_list
[5, 111]
>>> another_obj.another_list
[5, 420, 111]
>>> another_obj.another_list is SomeClass.another_list
True
>>> another_obj.another_list is some_obj.another_list
True
```

#### 💡 Объяснение:

* Переменная класса и переменные внутри экземпляра класса хранятся как словарь. Если имя переменной не найдено словаре текущего класса, тогда поиск производится по словарю базового класса.
* Оператор `+=` изменяет объект на месте, не создавая новый объект. Из-за этого изменение атрибута одного экземпляра влияет на остальные экземпляры.

---

### ▶ Нерефлексивный метод класса *


```py
	class SomeClass:
        def instance_method(self):
                pass
        
        @classmethod
        def class_method(cls):
                pass
```

**Вывод:**

```py
>>> SomeClass.instance_method is SomeClass.instance_method
True
>>> SomeClass.class_method is SomeClass.class_method
False
>>> id(SomeClass.class_method) == id(SomeClass.class_method)
True
```

#### 💡 Объяснение:

- Причина, по которой `SomeClass.class_method is SomeClass.class_method` является `False`, заключается в том, что у функции указан декоратор `@classmethod`. 

  ```py
  >>> SomeClass.instance_method
  <function __main__.SomeClass.instance_method(self)>
  >>> SomeClass.class_method
  <bound method SomeClass.class_method of <class '__main__.SomeClass'>
  ```

  A new bound method every time `SomeClass.class_method` is accessed.

-  `id(SomeClass.class_method) == id(SomeClass.class_method)` возвращает `True` из-за второго выделения памяти для `class_method`, которое происходит в том, же участке памяти, из которого была произведена первая очистка памяти. (Смотри пример "В глубине души мы все одинаковые"). 

---


### ▶ Генерируя пустоты
```py
some_iterable = ('a', 'b')

def some_func(val):
    return "something"
```

**Вывод (<= 3.7.x):**

```py
>>> [x for x in some_iterable]
['a', 'b']
>>> [(yield x) for x in some_iterable]
<generator object <listcomp> at 0x7f70b0a4ad58>
>>> list([(yield x) for x in some_iterable])
['a', 'b']
>>> list((yield x) for x in some_iterable)
['a', None, 'b', None]
>>> list(some_func((yield x)) for x in some_iterable)
['a', 'something', 'b', 'something']
```

#### 💡 Объяснение:
- Это баг в CPython при обработке `yield` в генераторах.
- Исходники с объяснениями находятся здесь: https://stackoverflow.com/questions/32139885/yield-in-list-comprehensions-and-generator-expressions
- Соответствующий bug report: http://bugs.python.org/issue10544
- В Python 3.8+ больше не разрешается использование `yield` внутри list comprehension, теперь это будет выбрасывать `SyntaxError`.

---


### ▶ Yielding from... вернёт! *
1\.

```py
def some_func(x):
    if x == 3:
        return ["wtf"]
    else:
        yield from range(x)
```

**Вывод (> 3.3):**

```py
>>> list(some_func(3))
[]
```

Куда делось `"wtf"`? Неужели это из-за эффекта `yield from`? Давайте узнаем,

2\.

```py
def some_func(x):
    if x == 3:
        return ["wtf"]
    else:
        for i in range(x):
          yield i
```

**Вывод:**

```py
>>> list(some_func(3))
[]
```

Тот же результат, снова не сработало.

#### 💡 Объяснение:

+ Начиная с Python 3.3 стало возможным использовать `return` внутри генераторов (Смотри [PEP380](https://www.python.org/dev/peps/pep-0380/)). [Официальная документация](https://www.python.org/dev/peps/pep-0380/#enhancements-to-stopiteration) говорит, что

> "... `return expr` in a generator causes `StopIteration(expr)` to be raised upon exit from the generator."

+ В случае с `some_func(3)`,  бросается исключение `StopIteration` в самом начале из-за `return`. Исключение `StopIteration` автоматически отлавливается внутри обёртки `list(...)` и цикла `for` . Поэтому оба примера выше возвращают пустые списки.

+ Чтобы получить `["wtf"]` из генератора `some_func`, нам нужно поймать исключение `StopIteration`,

  ```py
  try:
      next(some_func(3))
  except StopIteration as e:
      some_string = e.value
  ```

  ```py
  >>> some_string
  ["wtf"]
  ```

---

### ▶ NaN-рефлексивность

1\.

```py
a = float('inf')
b = float('nan')
c = float('-iNf')  # Эти строки регистро-независимы
d = float('nan')
```

**Вывод:**

```py
>>> a
inf
>>> b
nan
>>> c
-inf
>>> float('some_other_string')
ValueError: could not convert string to float: some_other_string
>>> a == -c # inf==inf
True
>>> None == None # None == None
True
>>> b == d # но nan!=nan
False
>>> 50 / a
0.0
>>> a / a
nan
>>> 23 + b
nan
```

2\.

```py
>>> x = float('nan')
>>> y = x / x
>>> y is y # Сохраняется идентичность
True
>>> y == y # сравнение не работает для переменной y
False
>>> [y] == [y] # но работает для списка с переменной y
True
```



#### 💡 Объяснение:

- `'inf'` и `'nan'` являютя специальными строками (регистро-независимыми), которые, при приведении к типу `float`, используются для представления  "бесконечности" и "не числа" соответственно.

- Согласно стандарту IEEE  `NaN != NaN`, соблюдение этого правила ломает рефлексивность элемента в коллекции в Python. Другими словами, если `x` это элемент коллекции, к примеру `list`, тогда некоторые операции, например сравнение, основываются на предположении, что `x == x`. Из-за этого предположения, сначала проверяется идентичность оператором `is` (так как это быстрее), а равенство проверяется только при получении неидентичной пары элементов. Следующий фрагмент кода проясняет ситуацию,

  ```py
  >>> x = float('nan')
  >>> x == x, [x] == [x]
  (False, True)
  >>> y = float('nan')
  >>> y == y, [y] == [y]
  (False, True)
  >>> x == y, [x] == [y]
  (False, False)
  ```

  Так как `x` неидентичен `y` (`(x is y) == False`), сравниваются значения, которые не равны, поэтому возвращается `False`.

- Интересная статья: [Рефлексивность и прочие столпы цивилизации](https://bertrandmeyer.com/2010/02/06/reflexivity-and-other-pillars-of-civilization/)

---

### ▶ Изменяя неизменяемое!

Это может показаться тривиальным, если знать, как работают ссылки в Python.

```py
some_tuple = ("A", "tuple", "with", "values")
another_tuple = ([1, 2], [3, 4], [5, 6])
```

**Вывод:**
```py
>>> some_tuple[2] = "change this"
TypeError: 'tuple' object does not support item assignment
>>> another_tuple[2].append(1000) # Ошибки не будет
>>> another_tuple
([1, 2], [3, 4], [5, 6, 1000])
>>> another_tuple[2] += [99, 999]
TypeError: 'tuple' object does not support item assignment
>>> another_tuple
([1, 2], [3, 4], [5, 6, 1000, 99, 999])
```

But I thought tuples were immutable...

#### 💡 Объяснение:

* Цитата из [документации](https://docs.python.org/2/reference/datamodel.html)

    > Immutable sequences
        An object of an immutable sequence type cannot change once it is created. (If the object contains references to other objects, these other objects may be mutable and may be modified; however, the collection of objects directly referenced by an immutable object cannot change.)

* Оператор `+=` изменяет существующий список. Присваивание не срабатывает, но к моменту исключения, существующий список уже был изменён.

---

### ▶ The disappearing variable from outer scope

```py
e = 7
try:
    raise Exception()
except Exception as e:
    pass
```

**Вывод (Python 2.x):**
```py
>>> print(e)
# prints nothing
```

**Вывод (Python 3.x):**
```py
>>> print(e)
NameError: name 'e' is not defined
```

#### 💡 Объяснение:

* Source: https://docs.python.org/3/reference/compound_stmts.html#except

  When an exception has been assigned using `as` target, it is cleared at the end of the `except` clause. This is as if

  ```py
  except E as N:
      foo
  ```

  was translated into

  ```py
  except E as N:
      try:
          foo
      finally:
          del N
  ```

  This means the exception must be assigned to a different name to be able to refer to it after the except clause. Exceptions are cleared because, with the traceback attached to them, they form a reference cycle with the stack frame, keeping all locals in that frame alive until the next garbage collection occurs.

* The clauses are not scoped in Python. Everything in the example is present in the same scope, and the variable `e` got removed due to the execution of the `except` clause. The same is not the case with functions that have their separate inner-scopes. The example below illustrates this:

     ```py
     def f(x):
         del(x)
         print(x)

     x = 5
     y = [5, 4, 3]
     ```

     **Вывод:**
     ```py
     >>>f(x)
     UnboundLocalError: local variable 'x' referenced before assignment
     >>>f(y)
     UnboundLocalError: local variable 'x' referenced before assignment
     >>> x
     5
     >>> y
     [5, 4, 3]
     ```

* In Python 2.x, the variable name `e` gets assigned to `Exception()` instance, so when you try to print, it prints nothing.

    **Вывод (Python 2.x):**
    ```py
    >>> e
    Exception()
    >>> print e
    # Nothing is printed!
    ```

---


### ▶ The mysterious key type conversion
```py
class SomeClass(str):
    pass

some_dict = {'s': 42}
```

**Вывод:**
```py
>>> type(list(some_dict.keys())[0])
str
>>> s = SomeClass('s')
>>> some_dict[s] = 40
>>> some_dict # expected: Two different keys-value pairs
{'s': 40}
>>> type(list(some_dict.keys())[0])
str
```

#### 💡 Объяснение:

* Both the object `s` and the string `"s"` hash to the same value because `SomeClass` inherits the `__hash__` method of `str` class.
* `SomeClass("s") == "s"` evaluates to `True` because `SomeClass` also inherits `__eq__` method from `str` class.
* Since both the objects hash to the same value and are equal, they are represented by the same key in the dictionary.
* For the desired behavior, we can redefine the `__eq__` method in `SomeClass`
  ```py
  class SomeClass(str):
    def __eq__(self, other):
        return (
            type(self) is SomeClass
            and type(other) is SomeClass
            and super().__eq__(other)
        )

    # When we define a custom __eq__, Python stops automatically inheriting the
    # __hash__ method, so we need to define it as well
    __hash__ = str.__hash__

  some_dict = {'s':42}
  ```

  **Вывод:**
  ```py
  >>> s = SomeClass('s')
  >>> some_dict[s] = 40
  >>> some_dict
  {'s': 40, 's': 42}
  >>> keys = list(some_dict.keys())
  >>> type(keys[0]), type(keys[1])
  (__main__.SomeClass, str)
  ```

---

### ▶ Let's see if you can guess this?
```py
a, b = a[b] = {}, 5
```

**Вывод:**
```py
>>> a
{5: ({...}, 5)}
```

#### 💡 Объяснение:

* According to [Python language reference](https://docs.python.org/2/reference/simple_stmts.html#assignment-statements), assignment statements have the form
  ```
  (target_list "=")+ (expression_list | yield_expression)
  ```
  and
  
> An assignment statement evaluates the expression list (remember that this can be a single expression or a comma-separated list, the latter yielding a tuple) and assigns the single resulting object to each of the target lists, from left to right.

* The `+` in `(target_list "=")+` means there can be **one or more** target lists. In this case, target lists are `a, b` and `a[b]` (note the expression list is exactly one, which in our case is `{}, 5`).

* After the expression list is evaluated, its value is unpacked to the target lists from **left to right**. So, in our case, first the `{}, 5` tuple is unpacked to `a, b` and we now have `a = {}` and `b = 5`.

* `a` is now assigned to `{}`, which is a mutable object.

* The second target list is `a[b]` (you may expect this to throw an error because both `a` and `b` have not been defined in the statements before. But remember, we just assigned `a` to `{}` and `b` to `5`).

* Now, we are setting the key `5` in the dictionary to the tuple `({}, 5)` creating a circular reference (the `{...}` in the output refers to the same object that `a` is already referencing). Another simpler example of circular reference could be
  ```py
  >>> some_list = some_list[0] = [0]
  >>> some_list
  [[...]]
  >>> some_list[0]
  [[...]]
  >>> some_list is some_list[0]
  True
  >>> some_list[0][0][0][0][0][0] == some_list
  True
  ```
  Similar is the case in our example (`a[b][0]` is the same object as `a`)

* So to sum it up, you can break the example down to
  ```py
  a, b = {}, 5
  a[b] = a, b
  ```
  And the circular reference can be justified by the fact that `a[b][0]` is the same object as `a`
  ```py
  >>> a[b][0] is a
  True
  ```

---
---

## Секция: Slippery Slopes

### ▶ Modifying a dictionary while iterating over it
```py
x = {0: None}

for i in x:
    del x[i]
    x[i+1] = None
    print(i)
```

**Вывод (Python 2.7- Python 3.5):**

```
0
1
2
3
4
5
6
7
```

Yes, it runs for exactly **eight** times and stops.

#### 💡 Объяснение:

* Iteration over a dictionary that you edit at the same time is not supported.
* It runs eight times because that's the point at which the dictionary resizes to hold more keys (we have eight deletion entries, so a resize is needed). This is actually an implementation detail.
* How deleted keys are handled and when the resize occurs might be different for different Python implementations.
* So for Python versions other than Python 2.7 - Python 3.5, the count might be different from 8 (but whatever the count is, it's going to be the same every time you run it). You can find some discussion around this [here](https://github.com/satwikkansal/wtfpython/issues/53) or in [this](https://stackoverflow.com/questions/44763802/bug-in-python-dict) StackOverflow thread.
* Python 3.8 onwards, you'll see `RuntimeError: dictionary keys changed during iteration` exception if you try to do this.

---

### ▶ Stubborn `del` operation

```py
class SomeClass:
    def __del__(self):
        print("Deleted!")
```

**Вывод:**
1\.
```py
>>> x = SomeClass()
>>> y = x
>>> del x # this should print "Deleted!"
>>> del y
Deleted!
```

Phew, deleted at last. You might have guessed what saved from `__del__` being called in our first attempt to delete `x`. Let's add more twists to the example.

2\.
```py
>>> x = SomeClass()
>>> y = x
>>> del x
>>> y # check if y exists
<__main__.SomeClass instance at 0x7f98a1a67fc8>
>>> del y # Like previously, this should print "Deleted!"
>>> globals() # oh, it didn't. Let's check all our global variables and confirm
Deleted!
{'__builtins__': <module '__builtin__' (built-in)>, 'SomeClass': <class __main__.SomeClass at 0x7f98a1a5f668>, '__package__': None, '__name__': '__main__', '__doc__': None}
```

Okay, now it's deleted :confused:

#### 💡 Объяснение:
+ `del x` doesn’t directly call `x.__del__()`.
+ Whenever `del x` is encountered, Python decrements the reference count for `x` by one, and `x.__del__()` when x’s reference count reaches zero.
+ In the second output snippet, `y.__del__()` was not called because the previous statement (`>>> y`) in the interactive interpreter created another reference to the same object, thus preventing the reference count from reaching zero when `del y` was encountered.
+ Calling `globals` caused the existing reference to be destroyed, and hence we can see "Deleted!" being printed (finally!).

---

### ▶ The out of scope variable
```py
a = 1
def some_func():
    return a

def another_func():
    a += 1
    return a
```

**Вывод:**
```py
>>> some_func()
1
>>> another_func()
UnboundLocalError: local variable 'a' referenced before assignment
```

#### 💡 Объяснение:
* When you make an assignment to a variable in scope, it becomes local to that scope. So `a` becomes local to the scope of `another_func`,  but it has not been initialized previously in the same scope, which throws an error.
* Read [this](http://sebastianraschka.com/Articles/2014_python_scope_and_namespaces.html) short but an awesome guide to learn more about how namespaces and scope resolution works in Python.
* To modify the outer scope variable `a` in `another_func`, use `global` keyword.
  ```py
  def another_func()
      global a
      a += 1
      return a
  ```

  **Вывод:**
  ```py
  >>> another_func()
  2
  ```

---

### ▶ Deleting a list item while iterating
```py
list_1 = [1, 2, 3, 4]
list_2 = [1, 2, 3, 4]
list_3 = [1, 2, 3, 4]
list_4 = [1, 2, 3, 4]

for idx, item in enumerate(list_1):
    del item

for idx, item in enumerate(list_2):
    list_2.remove(item)

for idx, item in enumerate(list_3[:]):
    list_3.remove(item)

for idx, item in enumerate(list_4):
    list_4.pop(idx)
```

**Вывод:**
```py
>>> list_1
[1, 2, 3, 4]
>>> list_2
[2, 4]
>>> list_3
[]
>>> list_4
[2, 4]
```

Can you guess why the output is `[2, 4]`?

#### 💡 Объяснение:

* It's never a good idea to change the object you're iterating over. The correct way to do so is to iterate over a copy of the object instead, and `list_3[:]` does just that.

     ```py
     >>> some_list = [1, 2, 3, 4]
     >>> id(some_list)
     139798789457608
     >>> id(some_list[:]) # Notice that python creates new object for sliced list.
     139798779601192
     ```

**Difference between `del`, `remove`, and `pop`:**
* `del var_name` just removes the binding of the `var_name` from the local or global namespace (That's why the `list_1` is unaffected).
* `remove` removes the first matching value, not a specific index, raises `ValueError` if the value is not found.
* `pop` removes the element at a specific index and returns it, raises `IndexError` if an invalid index is specified.

**Why the output is `[2, 4]`?**
- The list iteration is done index by index, and when we remove `1` from `list_2` or `list_4`, the contents of the lists are now `[2, 3, 4]`. The remaining elements are shifted down, i.e., `2` is at index 0, and `3` is at index 1. Since the next iteration is going to look at index 1 (which is the `3`), the `2` gets skipped entirely. A similar thing will happen with every alternate element in the list sequence.

* Refer to this StackOverflow [thread](https://stackoverflow.com/questions/45946228/what-happens-when-you-try-to-delete-a-list-element-while-iterating-over-it) explaining the example
* See also this nice StackOverflow [thread](https://stackoverflow.com/questions/45877614/how-to-change-all-the-dictionary-keys-in-a-for-loop-with-d-items) for a similar example related to dictionaries in Python.

---


### ▶ Lossy zip of iterators *

```py
>>> numbers = list(range(7))
>>> numbers
[0, 1, 2, 3, 4, 5, 6]
>>> first_three, remaining = numbers[:3], numbers[3:]
>>> first_three, remaining
([0, 1, 2], [3, 4, 5, 6])
>>> numbers_iter = iter(numbers)
>>> list(zip(numbers_iter, first_three)) 
[(0, 0), (1, 1), (2, 2)]
# so far so good, let's zip the remaining
>>> list(zip(numbers_iter, remaining))
[(4, 3), (5, 4), (6, 5)]
```
Where did element `3` go from the `numbers` list?

#### 💡 Объяснение:

- From Python [docs](https://docs.python.org/3.3/library/functions.html#zip), here's an approximate implementation of zip function,
    ```py
    def zip(*iterables):
        sentinel = object()
        iterators = [iter(it) for it in iterables]
        while iterators:
            result = []
            for it in iterators:
                elem = next(it, sentinel)
                if elem is sentinel: return
                result.append(elem)
            yield tuple(result)
    ```
- So the function takes in arbitrary number of itreable objects, adds each of their items to the `result` list by calling the `next` function on them, and stops whenever any of the iterable is exhausted. 
- The caveat here is when any iterable is exhausted, the existing elements in the `result` list are discarded. That's what happened with `3` in the `numbers_iter`.
- The correct way to do the above using `zip` would be,
    ```py
    >>> numbers = list(range(7))
    >>> numbers_iter = iter(numbers)
    >>> list(zip(first_three, numbers_iter))
    [(0, 0), (1, 1), (2, 2)]
    >>> list(zip(remaining, numbers_iter))
    [(3, 3), (4, 4), (5, 5), (6, 6)]
    ```
    The first argument of zip should be the one with fewest elements.

---

### ▶ Loop variables leaking out!
1\.
```py
for x in range(7):
    if x == 6:
        print(x, ': for x inside loop')
print(x, ': x in global')
```

**Вывод:**
```py
6 : for x inside loop
6 : x in global
```

But `x` was never defined outside the scope of for loop...

2\.
```py
# This time let's initialize x first
x = -1
for x in range(7):
    if x == 6:
        print(x, ': for x inside loop')
print(x, ': x in global')
```

**Вывод:**
```py
6 : for x inside loop
6 : x in global
```

3\.

**Вывод (Python 2.x):**
```py
>>> x = 1
>>> print([x for x in range(5)])
[0, 1, 2, 3, 4]
>>> print(x)
4
```

**Вывод (Python 3.x):**
```py
>>> x = 1
>>> print([x for x in range(5)])
[0, 1, 2, 3, 4]
>>> print(x)
1
```

#### 💡 Объяснение:

- In Python, for-loops use the scope they exist in and leave their defined loop-variable behind. This also applies if we explicitly defined the for-loop variable in the global namespace before. In this case, it will rebind the existing variable.

- The differences in the output of Python 2.x and Python 3.x interpreters for list comprehension example can be explained by following change documented in [What’s New In Python 3.0](https://docs.python.org/3/whatsnew/3.0.html) changelog:

    > "List comprehensions no longer support the syntactic form `[... for var in item1, item2, ...]`. Use `[... for var in (item1, item2, ...)]` instead. Also, note that list comprehensions have different semantics: they are closer to syntactic sugar for a generator expression inside a `list()` constructor, and in particular, the loop control variables are no longer leaked into the surrounding scope."

---

### ▶ Beware of default mutable arguments!

```py
def some_func(default_arg=[]):
    default_arg.append("some_string")
    return default_arg
```

**Вывод:**
```py
>>> some_func()
['some_string']
>>> some_func()
['some_string', 'some_string']
>>> some_func([])
['some_string']
>>> some_func()
['some_string', 'some_string', 'some_string']
```

#### 💡 Объяснение:

- The default mutable arguments of functions in Python aren't really initialized every time you call the function. Instead, the recently assigned value to them is used as the default value. When we explicitly passed `[]` to `some_func` as the argument, the default value of the `default_arg` variable was not used, so the function returned as expected.

    ```py
    def some_func(default_arg=[]):
        default_arg.append("some_string")
        return default_arg
    ```

    **Вывод:**
    ```py
    >>> some_func.__defaults__ #This will show the default argument values for the function
    ([],)
    >>> some_func()
    >>> some_func.__defaults__
    (['some_string'],)
    >>> some_func()
    >>> some_func.__defaults__
    (['some_string', 'some_string'],)
    >>> some_func([])
    >>> some_func.__defaults__
    (['some_string', 'some_string'],)
    ```

- A common practice to avoid bugs due to mutable arguments is to assign `None` as the default value and later check if any value is passed to the function corresponding to that argument. Example:

    ```py
    def some_func(default_arg=None):
        if default_arg is None:
            default_arg = []
        default_arg.append("some_string")
        return default_arg
    ```

---

### ▶ Catching the Exceptions
```py
some_list = [1, 2, 3]
try:
    # This should raise an ``IndexError``
    print(some_list[4])
except IndexError, ValueError:
    print("Caught!")

try:
    # This should raise a ``ValueError``
    some_list.remove(4)
except IndexError, ValueError:
    print("Caught again!")
```

**Вывод (Python 2.x):**
```py
Caught!

ValueError: list.remove(x): x not in list
```

**Вывод (Python 3.x):**
```py
  File "<input>", line 3
    except IndexError, ValueError:
                     ^
SyntaxError: invalid syntax
```

#### 💡 Объяснение:

* To add multiple Exceptions to the except clause, you need to pass them as parenthesized tuple as the first argument. The second argument is an optional name, which when supplied will bind the Exception instance that has been raised. Example,
  ```py
  some_list = [1, 2, 3]
  try:
     # This should raise a ``ValueError``
     some_list.remove(4)
  except (IndexError, ValueError), e:
     print("Caught again!")
     print(e)
  ```
  **Вывод (Python 2.x):**
  ```
  Caught again!
  list.remove(x): x not in list
  ```
  **Вывод (Python 3.x):**
  ```py
    File "<input>", line 4
      except (IndexError, ValueError), e:
                                       ^
  IndentationError: unindent does not match any outer indentation level
  ```

* Separating the exception from the variable with a comma is deprecated and does not work in Python 3; the correct way is to use `as`. Example,
  ```py
  some_list = [1, 2, 3]
  try:
      some_list.remove(4)

  except (IndexError, ValueError) as e:
      print("Caught again!")
      print(e)
  ```
  **Вывод:**
  ```
  Caught again!
  list.remove(x): x not in list
  ```

---

### ▶ Same operands, different story!
1\.
```py
a = [1, 2, 3, 4]
b = a
a = a + [5, 6, 7, 8]
```

**Вывод:**
```py
>>> a
[1, 2, 3, 4, 5, 6, 7, 8]
>>> b
[1, 2, 3, 4]
```

2\.
```py
a = [1, 2, 3, 4]
b = a
a += [5, 6, 7, 8]
```

**Вывод:**
```py
>>> a
[1, 2, 3, 4, 5, 6, 7, 8]
>>> b
[1, 2, 3, 4, 5, 6, 7, 8]
```

#### 💡 Объяснение:

*  `a += b` doesn't always behave the same way as `a = a + b`.  Classes *may* implement the *`op=`* operators differently, and lists do this.

* The expression `a = a + [5,6,7,8]` generates a new list and sets `a`'s reference to that new list, leaving `b` unchanged.

* The expression `a += [5,6,7,8]` is actually mapped to an "extend" function that operates on the list such that `a` and `b` still point to the same list that has been modified in-place.

---

### ▶ Name resolution ignoring class scope
1\.
```py
x = 5
class SomeClass:
    x = 17
    y = (x for i in range(10))
```

**Вывод:**
```py
>>> list(SomeClass.y)[0]
5
```

2\.
```py
x = 5
class SomeClass:
    x = 17
    y = [x for i in range(10)]
```

**Вывод (Python 2.x):**
```py
>>> SomeClass.y[0]
17
```

**Вывод (Python 3.x):**
```py
>>> SomeClass.y[0]
5
```

#### 💡 Объяснение:
- Scopes nested inside class definition ignore names bound at the class level.
- A generator expression has its own scope.
- Starting from Python 3.X, list comprehensions also have their own scope.

---

### ▶ Needles in a Haystack *


I haven't met even a single experience Pythonist till date who has not come across one or more of the following scenarios,

1\.

```py
x, y = (0, 1) if True else None, None
```

**Вывод:**

```py
>>> x, y  # expected (0, 1)
((0, 1), None)
```

2\.

```py
t = ('one', 'two')
for i in t:
    print(i)

t = ('one')
for i in t:
    print(i)

t = ()
print(t)
```

**Вывод:**

```py
one
two
o
n
e
tuple()
```

3\.

```
ten_words_list = [
    "some",
    "very",
    "big",
    "list",
    "that"
    "consists",
    "of",
    "exactly",
    "ten",
    "words"
]
```

**Вывод**

```py
>>> len(ten_words_list)
9
```

4\. Not asserting strongly enough

```py
a = "python"
b = "javascript"
```

**Вывод:**

```py
# An assert statement with an assertion failure message.
>>> assert(a == b, "Both languages are different")
# No AssertionError is raised
```

5\.

```py
some_list = [1, 2, 3]
some_dict = {
  "key_1": 1,
  "key_2": 2,
  "key_3": 3
}

some_list = some_list.append(4) 
some_dict = some_dict.update({"key_4": 4})
```

**Вывод:**

```py
>>> print(some_list)
None
>>> print(some_dict)
None
```

6\.

```py
def some_recursive_func(a):
    if a[0] == 0:
        return 
    a[0] -= 1
    some_recursive_func(a)
    return a

def similar_recursive_func(a):
        if a == 0:
                return a
        a -= 1
        similar_recursive_func(a)
        return a
```

**Вывод:**

```py
>>> some_recursive_func([5, 0])
[0, 0]
>>> similar_recursive_func(5)
4
```

#### 💡 Объяснение:

* For 1, the correct statement for expected behavior is `x, y = (0, 1) if True else (None, None)`.

* For 2, the correct statement for expected behavior is `t = ('one',)` or `t = 'one',` (missing comma) otherwise the interpreter considers `t` to be a `str` and iterates over it character by character.

* `()` is a special token and denotes empty `tuple`.

* In 3, as you might have already figured out, there's a missing comma after 5th element (`"that"`) in the list. So by implicit string literal concatenation,

  ```py
  >>> ten_words_list
  ['some', 'very', 'big', 'list', 'thatconsists', 'of', 'exactly', 'ten', 'words']
  ```

* No `AssertionError` was raised in 4th snippet because instead of asserting the individual expression `a == b`, we're asserting entire tuple. The following snippet will clear things up,

  ```py
  >>> a = "python"
  >>> b = "javascript"
  >>> assert a == b
  Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
  AssertionError
  
  >>> assert (a == b, "Values are not equal")
  <stdin>:1: SyntaxWarning: assertion is always true, perhaps remove parentheses?
  
  >>> assert a == b, "Values are not equal"
  Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
  AssertionError: Values aren not equal
  ```

* As for the fifth snippet, most methods that modify the items of sequence/mapping objects like `list.append`, `dict.update`, `list.sort`, etc. modify the objects in-place and return `None`. The rationale behind this is to improve performance by avoiding making a copy of the object if the operation can be done in-place (Referred from [here](http://docs.python.org/2/faq/design.html#why-doesn-t-list-sort-return-the-sorted-list)).

* Last one should be fairly obvious, mutable object (like `list`) can be altered in the function, and the reassignation of an immutable (`a -= 1`) is not an alteration of the value.

* Being aware of these nitpicks can save you hours of debugging effort in the long run. 

---


### ▶ Splitsies *
```py
>>> 'a'.split()
['a']

# is same as
>>> 'a'.split(' ')
['a']

# but
>>> len(''.split())
0

# isn't the same as
>>> len(''.split(' '))
1
```

#### 💡 Объяснение:

- It might appear at first that the default separator for split is a single space `' '`, but as per the [docs](https://docs.python.org/2.7/library/stdtypes.html#str.split)
    >  If sep is not specified or is `None`, a different splitting algorithm is applied: runs of consecutive whitespace are regarded as a single separator, and the result will contain no empty strings at the start or end if the string has leading or trailing whitespace. Consequently, splitting an empty string or a string consisting of just whitespace with a None separator returns `[]`.
    > If sep is given, consecutive delimiters are not grouped together and are deemed to delimit empty strings (for example, `'1,,2'.split(',')` returns `['1', '', '2']`). Splitting an empty string with a specified separator returns `['']`.
- Noticing how the leading and trailing whitespaces are handled in the following snippet will make things clear,
    ```py
    >>> ' a '.split(' ')
    ['', 'a', '']
    >>> ' a '.split()
    ['a']
    >>> ''.split(' ')
    ['']
    ```

---

### ▶ Wild imports *

```py
# File: module.py

def some_weird_name_func_():
    print("works!")

def _another_weird_name_func():
    print("works!")

```

**Вывод**

```py
>>> from module import *
>>> some_weird_name_func_()
"works!"
>>> _another_weird_name_func()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name '_another_weird_name_func' is not defined
```

#### 💡 Объяснение:

- It is often advisable to not use wildcard imports. The first obvious reason for this is, in wildcard imports, the names with a leading underscore don't get imported. This may lead to errors during runtime.
- Had we used `from ... import a, b, c` syntax, the above `NameError` wouldn't have occurred.
    ```py
    >>> from module import some_weird_name_func_, _another_weird_name_func
    >>> _another_weird_name_func()
    works!
    ```
- If you really want to use wildcard imports, then you'd have to define the list `__all__` in your module that will contain a list of public objects that'll be available when we do wildcard imports.
    ```py
    __all__ = ['_another_weird_name_func']

    def some_weird_name_func_():
        print("works!")

    def _another_weird_name_func():
        print("works!")
    ```
    **Вывод**

    ```py
    >>> _another_weird_name_func()
    "works!"
    >>> some_weird_name_func_()
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'some_weird_name_func_' is not defined
    ```

---

### ▶ All sorted? *


```py
>>> x = 7, 8, 9
>>> sorted(x) == x
False
>>> sorted(x) == sorted(x)
True

>>> y = reversed(x)
>>> sorted(y) == sorted(y)
False
```

#### 💡 Объяснение:

- The `sorted` method always returns a list, and comparing lists and tuples always returns `False` in Python. 

- ```py
  >>> [] == tuple()
  False
  >>> x = 7, 8, 9
  >>> type(x), type(sorted(x))
  (tuple, list)
  ```

- Unlike `sorted`, the `reversed` method returns an iterator. Why? Because sorting requires the iterator to be either modified in-place or use an extra container (a list), whereas reversing can simply work by iterating from the last index to the first.

- So during comparison `sorted(y) == sorted(y)`, the first call to `sorted()` will consume the iterator `y`, and the next call will just return an empty list.

  ```py
  >>> x = 7, 8, 9
  >>> y = reversed(x)
  >>> sorted(y), sorted(y)
  ([7, 8, 9], [])
  ```

---

### ▶ Midnight time doesn't exist?
```py
from datetime import datetime

midnight = datetime(2018, 1, 1, 0, 0)
midnight_time = midnight.time()

noon = datetime(2018, 1, 1, 12, 0)
noon_time = noon.time()

if midnight_time:
    print("Time at midnight is", midnight_time)

if noon_time:
    print("Time at noon is", noon_time)
```

**Вывод (< 3.5):**

```py
('Time at noon is', datetime.time(12, 0))
```
The midnight time is not printed.

#### 💡 Объяснение:

Before Python 3.5, the boolean value for `datetime.time` object was considered to be `False` if it represented midnight in UTC. It is error-prone when using the `if obj:` syntax to check if the `obj` is null or some equivalent of "empty."

---
---



## Секция: The Hidden treasures!

This section contains a few lesser-known and interesting things about Python that most beginners like me are unaware of (well, not anymore).

### ▶ Okay Python, Can you make me fly?
Well, here you go

```py
import antigravity
```

**Вывод:**
Sshh... It's a super-secret.

#### 💡 Объяснение:
+ `antigravity` module is one of the few easter eggs released by Python developers.
+ `import antigravity` opens up a web browser pointing to the [classic XKCD comic](http://xkcd.com/353/) about Python.
+ Well, there's more to it. There's **another easter egg inside the easter egg**. If you look at the [code](https://github.com/python/cpython/blob/master/Lib/antigravity.py#L7-L17), there's a function defined that purports to implement the [XKCD's geohashing algorithm](https://xkcd.com/426/).

---

### ▶ `goto`, but why?

```py
from goto import goto, label
for i in range(9):
    for j in range(9):
        for k in range(9):
            print("I am trapped, please rescue!")
            if k == 2:
                goto .breakout # breaking out from a deeply nested loop
label .breakout
print("Freedom!")
```

**Вывод (Python 2.3):**
```py
I am trapped, please rescue!
I am trapped, please rescue!
Freedom!
```

#### 💡 Объяснение:
- A working version of `goto` in Python was [announced](https://mail.python.org/pipermail/python-announce-list/2004-April/002982.html) as an April Fool's joke on 1st April 2004.
- Current versions of Python do not have this module.
- Although it works, but please don't use it. Here's the [reason](https://docs.python.org/3/faq/design.html#why-is-there-no-goto) to why `goto` is not present in Python.

---

### ▶ Brace yourself!
If you are one of the people who doesn't like using whitespace in Python to denote scopes, you can use the C-style {} by importing,

```py
from __future__ import braces
```

**Вывод:**
```py
  File "some_file.py", line 1
    from __future__ import braces
SyntaxError: not a chance
```

Braces? No way! If you think that's disappointing, use Java. Okay, another surprising thing, can you find where's the `SyntaxError` raised in `__future__` module [code](https://github.com/python/cpython/blob/master/Lib/__future__.py)?

#### 💡 Объяснение:
+ The `__future__` module is normally used to provide features from future versions of Python. The "future" in this specific context is however, ironic.
+ This is an easter egg concerned with the community's feelings on this issue.
+ The code is actually present [here](https://github.com/python/cpython/blob/025eb98dc0c1dc27404df6c544fc2944e0fa9f3a/Python/future.c#L49) in `future.c` file.
+ When the CPython compiler encounters a [future statement](https://docs.python.org/3.3/reference/simple_stmts.html#future-statements), it first runs the appropriate code in `future.c` before treating it as a normal import statement.

---

### ▶ Let's meet Friendly Language Uncle For Life
**Вывод (Python 3.x)**
```py
>>> from __future__ import barry_as_FLUFL
>>> "Ruby" != "Python" # there's no doubt about it
  File "some_file.py", line 1
    "Ruby" != "Python"
              ^
SyntaxError: invalid syntax

>>> "Ruby" <> "Python"
True
```

There we go.

#### 💡 Объяснение:
- This is relevant to [PEP-401](https://www.python.org/dev/peps/pep-0401/) released on April 1, 2009 (now you know, what it means).
- Quoting from the PEP-401
  
  > Recognized that the != inequality operator in Python 3.0 was a horrible, finger-pain inducing mistake, the FLUFL reinstates the <> diamond operator as the sole spelling.
- There were more things that Uncle Barry had to share in the PEP; you can read them [here](https://www.python.org/dev/peps/pep-0401/).
- It works well in an interactive environment, but it will raise a `SyntaxError` when you run via python file (see this [issue](https://github.com/satwikkansal/wtfpython/issues/94)). However, you can wrap the statement inside an `eval` or `compile` to get it working,
    ```py
    from __future__ import barry_as_FLUFL
    print(eval('"Ruby" <> "Python"'))
    ```

---

### ▶ Даже Python понимает, что любовь это сложно
```py
import this
```

Подождите, что за **this**? `this` is love :heart:

**Вывод:**
```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

Это дзен Python!

```py
>>> love = this
>>> this is love
True
>>> love is True
False
>>> love is False
False
>>> love is not True or False
True
>>> love is not True or False; love is love  # Любовь это сложно
True
```

#### 💡 Объяснение:

* Модуль `this`  в Python это пасхался для дзена Python ([PEP 20](https://www.python.org/dev/peps/pep-0020)).
* And if you think that's already interesting enough, check out the implementation of [this.py](https://hg.python.org/cpython/file/c3896275c0f6/Lib/this.py). Interestingly, **the code for the Zen violates itself** (and that's probably the only place where this happens).
* Regarding the statement `love is not True or False; love is love`, ironic but it's self-explanatory (if not, please see the examples related to `is` and `is not` operators).

---

### ▶ Yes, it exists!
**The `else` clause for loops.** One typical example might be:

```py
  def does_exists_num(l, to_find):
      for num in l:
          if num == to_find:
              print("Exists!")
              break
      else:
          print("Does not exist")
```

**Вывод:**
```py
>>> some_list = [1, 2, 3, 4, 5]
>>> does_exists_num(some_list, 4)
Exists!
>>> does_exists_num(some_list, -1)
Does not exist
```

**The `else` clause in exception handling.** An example,

```py
try:
    pass
except:
    print("Exception occurred!!!")
else:
    print("Try block executed successfully...")
```

**Вывод:**
```py
Try block executed successfully...
```

#### 💡 Объяснение:
- The `else` clause after a loop is executed only when there's no explicit `break` after all the iterations. You can think of it as a "nobreak" clause.
- `else` clause after a try block is also called "completion clause" as reaching the `else` clause in a `try` statement means that the try block actually completed successfully.

---
### ▶ Ellipsis *
```py
def some_func():
    Ellipsis
```

**Вывод**
```py
>>> some_func()
# No output, No Error

>>> SomeRandomString
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'SomeRandomString' is not defined

>>> Ellipsis
Ellipsis
```

#### 💡 Объяснение:
- In Python, `Ellipsis` is a globally available built-in object which is equivalent to `...`.
    ```py
    >>> ...
    Ellipsis
    ```
- Eliipsis can be used for several purposes,
    + As a placeholder for code that hasn't been written yet (just like `pass` statement)
    + In slicing syntax to represent the full slices in remaining direction
    ```py
    >>> import numpy as np
    >>> three_dimensional_array = np.arange(8).reshape(2, 2, 2)
    array([
        [
            [0, 1],
            [2, 3]
        ],

        [
            [4, 5],
            [6, 7]
        ]
    ])
    ```
    So our `three_dimensional_array` is an array of array of arrays. Let's say we want to print the second element (index `1`) of all the innermost arrays, we can use Ellipsis to bypass all the preceding dimensions
    ```py
    >>> three_dimensional_array[:,:,1]
    array([[1, 3],
       [5, 7]])
    >>> three_dimensional_array[..., 1] # using Ellipsis.
    array([[1, 3],
       [5, 7]])
    ```
    Примечание: this will work for any number of dimensions. You can even select slice in first and last dimension and ignore the middle ones this way (`n_dimensional_array[firs_dim_slice, ..., last_dim_slice]`)
    + In [type hinting](https://docs.python.org/3/library/typing.html) to indicate only a part of the type (like `(Callable[..., int]` or `Tuple[str, ...]`))
    + You may also use Ellipsis as a default function argument (in the cases when you want to differentiate between the "no argument passed" and "None value passed" scenarios).

---

### ▶ Inpinity
The spelling is intended. Please, don't submit a patch for this.

**Вывод (Python 3.x):**
```py
>>> infinity = float('infinity')
>>> hash(infinity)
314159
>>> hash(float('-inf'))
-314159
```

#### 💡 Объяснение:
- Hash of infinity is 10⁵ x π.
- Interestingly, the hash of `float('-inf')` is "-10⁵ x π" in Python 3, whereas "-10⁵ x e" in Python 2.

---

### ▶ Let's mangle
1\.
```py
class Yo(object):
    def __init__(self):
        self.__honey = True
        self.bro = True
```

**Вывод:**
```py
>>> Yo().bro
True
>>> Yo().__honey
AttributeError: 'Yo' object has no attribute '__honey'
>>> Yo()._Yo__honey
True
```

2\.
```py
class Yo(object):
    def __init__(self):
        # Let's try something symmetrical this time
        self.__honey__ = True
        self.bro = True
```

**Вывод:**
```py
>>> Yo().bro
True

>>> Yo()._Yo__honey__
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'Yo' object has no attribute '_Yo__honey__'
```

Why did `Yo()._Yo__honey` work?

3\.

```py
_A__variable = "Some value"

class A(object):
    def some_func(self):
        return __variable # not initialized anywhere yet
```

**Вывод:**
```py
>>> A().__variable
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'A' object has no attribute '__variable'

>>> A().some_func()
'Some value'
```


#### 💡 Объяснение:

* [Name Mangling](https://en.wikipedia.org/wiki/Name_mangling) is used to avoid naming collisions between different namespaces.
* In Python, the interpreter modifies (mangles) the class member names starting with `__` (double underscore a.k.a "dunder") and not ending with more than one trailing underscore by adding `_NameOfTheClass` in front.
* So, to access `__honey` attribute in the first snippet, we had to append `_Yo` to the front, which would prevent conflicts with the same name attribute defined in any other class.
* But then why didn't it work in the second snippet? Because name mangling excludes the names ending with double underscores.
* The third snippet was also a consequence of name mangling. The name `__variable` in the statement `return __variable` was mangled to `_A__variable`, which also happens to be the name of the variable we declared in the outer scope.
* Also, if the mangled name is longer than 255 characters, truncation will happen.

---
---

## Секция: Appearances are deceptive!

### ▶ Пропуск строчек?
**Вывод:**
```py
>>> value = 11
>>> valuе = 32
>>> value
11
```

Что случилсь?

**Примечание:** Самый просой способ воспроизвести это поведение - скопировать выражения выше и вставить их в свой интерпретатор или скрипт.

#### 💡 Объяснение:

Некоторые символы выглядят идентично буквам английского алфавита, но интерпретатор видит разницу.

```py
>>> ord('е') # Кириллическая буква 'e'
1077
>>> ord('e') # Латинская буква 'e', используемая стндартной клавиатурой
101
>>> 'е' == 'e'
False

>>> value = 42 # Латинская 'e'
>>> valuе = 23 # Кириллическая 'e', интерпретатор Python версии 2.x выдаст ошибку `SyntaxError`
>>> value
42
```

Встроенная функция `ord()` возвращает Unicode [code point](https://en.wikipedia.org/wiki/Code_point) для символа. Различные значения для латинской и криллической букв подтверждают поведение примера.

---

### ▶ Телепорт


```py
# `pip install numpy` first.
import numpy as np

def energy_send(x):
    # Инициализация массива numpy
    np.array([float(x)])

def energy_receive():
    # Возвращаем пустой numpy массив
    return np.empty((), dtype=np.float).tolist()
```

**Вывод:**
```py
>>> energy_send(123.456)
>>> energy_receive()
123.456
```

Ждём Нобелевскую премию?

#### 💡 Объяснение:

* Notice that the numpy array created in the `energy_send` function is not returned, so that memory space is free to reallocate.
* `numpy.empty()` returns the next free memory slot without reinitializing it. This memory spot just happens to be the same one that was just freed (usually, but not always).

---

### ▶ Well, something is fishy...
```py
def square(x):
    """
    A simple function to calculate the square of a number by addition.
    """
    sum_so_far = 0
    for counter in range(x):
        sum_so_far = sum_so_far + x
  return sum_so_far
```

**Вывод (Python 2.x):**

```py
>>> square(10)
10
```

Shouldn't that be 100?

**Примечание:** If you're not able to reproduce this, try running the file [mixed_tabs_and_spaces.py](/mixed_tabs_and_spaces.py) via the shell.

#### 💡 Объяснение:

* **Don't mix tabs and spaces!** The character just preceding return is a "tab",  and the code is indented by multiple of "4 spaces" elsewhere in the example.
* This is how Python handles tabs:
  
  > First, tabs are replaced (from left to right) by one to eight spaces such that the total number of characters up to and including the replacement is a multiple of eight <...>
* So the "tab" at the last line of `square` function is replaced with eight spaces, and it gets into the loop.
* Python 3 is kind enough to throw an error for such cases automatically.

    **Вывод (Python 3.x):**
    ```py
    TabError: inconsistent use of tabs and spaces in indentation
    ```

---
---

## Секция: Miscellaneous


### ▶ `+=` is faster

```py
# using "+", three strings:
>>> timeit.timeit("s1 = s1 + s2 + s3", setup="s1 = ' ' * 100000; s2 = ' ' * 100000; s3 = ' ' * 100000", number=100)
0.25748300552368164
# using "+=", three strings:
>>> timeit.timeit("s1 += s2 + s3", setup="s1 = ' ' * 100000; s2 = ' ' * 100000; s3 = ' ' * 100000", number=100)
0.012188911437988281
```

#### 💡 Объяснение:
+ `+=` is faster than `+` for concatenating more than two strings because the first string (example, `s1` for `s1 += s2 + s3`) is not destroyed while calculating the complete string.

---

### ▶ Let's make a giant string!
```py
def add_string_with_plus(iters):
    s = ""
    for i in range(iters):
        s += "xyz"
    assert len(s) == 3*iters

def add_bytes_with_plus(iters):
    s = b""
    for i in range(iters):
        s += b"xyz"
    assert len(s) == 3*iters

def add_string_with_format(iters):
    fs = "{}"*iters
    s = fs.format(*(["xyz"]*iters))
    assert len(s) == 3*iters

def add_string_with_join(iters):
    l = []
    for i in range(iters):
        l.append("xyz")
    s = "".join(l)
    assert len(s) == 3*iters

def convert_list_to_string(l, iters):
    s = "".join(l)
    assert len(s) == 3*iters
```

**Вывод:**

```py
# Executed in ipython shell using %timeit for better readability of results.
# You can also use the timeit module in normal python shell/scriptm=, example usage below
# timeit.timeit('add_string_with_plus(10000)', number=1000, globals=globals())

>>> NUM_ITERS = 1000
>>> %timeit -n1000 add_string_with_plus(NUM_ITERS)
124 µs ± 4.73 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
>>> %timeit -n1000 add_bytes_with_plus(NUM_ITERS)
211 µs ± 10.5 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_format(NUM_ITERS)
61 µs ± 2.18 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_join(NUM_ITERS)
117 µs ± 3.21 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> l = ["xyz"]*NUM_ITERS
>>> %timeit -n1000 convert_list_to_string(l, NUM_ITERS)
10.1 µs ± 1.06 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

Let's increase the number of iterations by a factor of 10.

```py
>>> NUM_ITERS = 10000
>>> %timeit -n1000 add_string_with_plus(NUM_ITERS) # Linear increase in execution time
1.26 ms ± 76.8 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_bytes_with_plus(NUM_ITERS) # Quadratic increase
6.82 ms ± 134 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_format(NUM_ITERS) # Linear increase
645 µs ± 24.5 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> %timeit -n1000 add_string_with_join(NUM_ITERS) # Linear increase
1.17 ms ± 7.25 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
>>> l = ["xyz"]*NUM_ITERS
>>> %timeit -n1000 convert_list_to_string(l, NUM_ITERS) # Linear increase
86.3 µs ± 2 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

#### 💡 Объяснение:
- Вы можете узнать больше про [timeit](https://docs.python.org/3/library/timeit.html) или [%timeit](https://ipython.org/ipython-doc/dev/interactive/magics.html#magic-timeit) по этим ссылкам. Они используются для замеров времени выполняемого кода.
- Не используйте  `+` для генерации длинных строк. В питоне, тип  `str` является неизменяемым, поэтому левая и правая строка копируются в новуб объединённую для каждой новой пары конкатенируемых строк. Если вы скаладываете 4 строки длиной в 10 символов, копирование символо произойдёт (10+10) + ((10+10)+10) + (((10+10)+10)+10) = 90 раз, вместо оптимальных 40 раз. Сложность возрастает с квадратической зависимостью от количества строк и их длины. (Это подтверждается временем выполнения функции `add_bytes_with_plus`)
- Следовательно, лучше использовать  `.format.` или синтаксис `%` (Однако для очень коротких строк они медленее, чем конкатенация через  `+`).
- Ещё лучше, если склеиваемые строки уже доступны Or better, if already you've contents available in the form of an iterable object, then use `''.join(iterable_object)` which is much faster.
- Unlike `add_bytes_with_plus` because of the `+=` optimizations discussed in the previous example, `add_string_with_plus` didn't show a quadratic increase in execution time. Had the statement been `s = s + "x" + "y" + "z"` instead of `s += "xyz"`, the increase would have been quadratic.
  ```py
  def add_string_with_plus(iters):
      s = ""
      for i in range(iters):
          s = s + "x" + "y" + "z"
      assert len(s) == 3*iters

  >>> %timeit -n100 add_string_with_plus(1000)
  388 µs ± 22.4 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
  >>> %timeit -n100 add_string_with_plus(10000) # Quadratic increase in execution time
  9 ms ± 298 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
  ```
- So many ways to format and create a giant string are somewhat in contrast to the [Zen of Python](https://www.python.org/dev/peps/pep-0020/), according to which,
  
    > There should be one-- and preferably only one --obvious way to do it.

---

### ▶ Minor Ones *
* `join()` is a string operation instead of list operation. (sort of counter-intuitive at first usage)

  **💡 Объяснение:** If `join()` is a method on a string, then it can operate on any iterable (list, tuple, iterators). If it were a method on a list, it'd have to be implemented separately by every type. Also, it doesn't make much sense to put a string-specific method on a generic `list` object API.
  
* Few weird looking but semantically correct statements:
  + `[] = ()` is a semantically correct statement (unpacking an empty `tuple` into an empty `list`)
  + `'a'[0][0][0][0][0]` is also a semantically correct statement as strings are [sequences](https://docs.python.org/3/glossary.html#term-sequence)(iterables supporting element access using integer indices) in Python.
  + `3 --0-- 5 == 8` and `--5 == 5` are both semantically correct statements and evaluate to `True`.

* Given that `a` is a number, `++a` and `--a` are both valid Python statements but don't behave the same way as compared with similar statements in languages like C, C++, or Java.
  ```py
  >>> a = 5
  >>> a
  5
  >>> ++a
  5
  >>> --a
  5
  ```

  **💡 Объяснение:**
  + There is no `++` operator in Python grammar. It is actually two `+` operators.
  + `++a` parses as `+(+a)` which translates to `a`. Similarly, the output of the statement `--a` can be justified.
  + This StackOverflow [thread](https://stackoverflow.com/questions/3654830/why-are-there-no-and-operators-in-python) discusses the rationale behind the absence of increment and decrement operators in Python.

* You must be aware of the Walrus operator in Python. But have you ever heard about *the space-invader operator*?
  ```py
  >>> a = 42
  >>> a -=- 1
  >>> a
  43
  ```
  It is used as an alternative incrementation operator, together with another one
  ```py
  >>> a +=+ 1
  >>> a
  >>> 44
  ```
  **💡 Объяснение:** This prank comes from [Raymond Hettinger's tweet](https://twitter.com/raymondh/status/1131103570856632321?lang=en). The space invader operator is actually just a malformatted `a -= (-1)`. Which is equivalent to `a = a - (- 1)`. Similar for the `a += (+ 1)` case.
  
* Python has an undocumented [converse implication](https://en.wikipedia.org/wiki/Converse_implication) operator. 
     
     ```py
     >>> False ** False == True
     True
     >>> False ** True == False
     True
     >>> True ** False == True
     True
     >>> True ** True == True
     True
     ```

     **💡 Объяснение:** If you replace `False` and `True` by 0 and 1 and do the maths, the truth table is equivalent to a converse implication operator. ([Source](https://github.com/cosmologicon/pywat/blob/master/explanation.md#the-undocumented-converse-implication-operator))
     
* Since we are talking operators, there's also `@` operator for matrix multiplication (don't worry, this time it's for real).

     ```py
     >>> import numpy as np
     >>> np.array([2, 2, 2]) @ np.array([7, 8, 8])
     46
     ```

     **💡 Объяснение:** The `@` operator was added in Python 3.5 keeping the scientific community in mind. Any object can overload `__matmul__` magic method to define behavior for this operator.

* From Python 3.8 onwards you can use a typical f-string syntax like `f'{some_var=}` for quick debugging. Example,
    ```py
    >>> some_string = "wtfpython"
    >>> f'{some_string=}'
    "some_string='wtfpython'"
    ``` 

* Python uses 2 bytes for local variable storage in functions. In theory, this means that only 65536 variables can be defined in a function. However, python has a handy solution built in that can be used to store more than 2^16 variable names. The following code demonstrates what happens in the stack when more than 65536 local variables are defined (Warning: This code prints around 2^18 lines of text, so be prepared!):
     
     ```py
     import dis
    exec("""
    def f():
        """ + """
        """.join(["X" + str(x) + "=" + str(x) for x in range(65539)]))

    f()

    print(dis.dis(f))
    ```
     
* Multiple Python threads won't run your *Python code* concurrently (yes, you heard it right!). It may seem intuitive to spawn several threads and let them execute your Python code concurrently, but, because of the [Global Interpreter Lock](https://wiki.python.org/moin/GlobalInterpreterLock) in Python, all you're doing is making your threads execute on the same core turn by turn. Python threads are good for IO-bound tasks, but to achieve actual parallelization in Python for CPU-bound tasks, you might want to use the Python [multiprocessing](https://docs.python.org/2/library/multiprocessing.html) module.

* Sometimes, the `print` method might not print values immediately. For example,

     ```py
     # File some_file.py
     import time
     
     print("wtfpython", end="_")
     time.sleep(3)
     ```

     This will print the `wtfpython` after 10 seconds due to the `end` argument because the output buffer is flushed either after encountering `\n` or when the program finishes execution. We can force the buffer to flush by passing `flush=True` argument.

* List slicing with out of the bounds indices throws no errors
  ```py
  >>> some_list = [1, 2, 3, 4, 5]
  >>> some_list[111:]
  []
  ```

* Slicing an iterable not always creates a new object. For example,
    ```py
    >>> some_str = "wtfpython"
    >>> some_list = ['w', 't', 'f', 'p', 'y', 't', 'h', 'o', 'n']
    >>> some_list is some_list[:] # False expected because a new object is created.
    False
    >>> some_str is some_str[:] # True because strings are immutable, so making a new object is of not much use.
    True
    ```

* `int('١٢٣٤٥٦٧٨٩')` returns `123456789` in Python 3. In Python, Decimal characters include digit characters, and all characters that can be used to form decimal-radix numbers, e.g. U+0660, ARABIC-INDIC DIGIT ZERO. Here's an [interesting story](http://chris.improbable.org/2014/8/25/adventures-in-unicode-digits/) related to this behavior of Python.

* You can separate numeric literals with underscores (for better readability) from Python 3 onwards.

     ```py
     >>> six_million = 6_000_000
     >>> six_million
     6000000
     >>> hex_address = 0xF00D_CAFE
     >>> hex_address
     4027435774
     ```

* `'abc'.count('') == 4`. Here's an approximate implementation of `count` method, which would make the things more clear
  ```py
  def count(s, sub):
      result = 0
      for i in range(len(s) + 1 - len(sub)):
          result += (s[i:i + len(sub)] == sub)
      return result
  ```
  The behavior is due to the matching of empty substring(`''`) with slices of length 0 in the original string.

---
---

# Сотрудничество

Несколько способов, которыми вы можете помочь wtfpython,

- Предлагать новые примеры
- Помочь с переводом (Смотри [issues с тегом translation](https://github.com/satwikkansal/wtfpython/issues?q=is%3Aissue+is%3Aopen+label%3Atranslation))
- Небольшие изменения, например поиск неактуальных примеров, опечаток, ошибок форматирования и т.д.
- Выявление пробелов. Например, неадекватных объяснений, избыточных примеров и т.д.
- Любые креативные предложения, чтобы сделать этот проект веселее и полезнее.

Также посмотрите [CONTRIBUTING.md](/CONTRIBUTING.md) для подробной информации. Не стесняйтесь открыть новую [issue](https://github.com/satwikkansal/wtfpython/issues/new) для обсуждений.

PS: Пожалуйста не обращайтесь с запросами размещения своих ссылок. Ссылки не будут добавлены, если они не имеют отношения к проекту.

# Благодарности

Идея и дизайн этой коллекции были первоначально вдохновлены Денисом Довханом и его замечательным проектом [wtfjs](https://github.com/denysdovhan/wtfjs), а впечатляющая поддержка Python сообщества привела проект в форму, в которой он сейчас и находится.

#### Несколько классных ссылок!
* https://www.youtube.com/watch?v=sH4XF6pKKmk
* https://www.reddit.com/r/Python/comments/3cu6ej/what_are_some_wtf_things_about_python
* https://sopython.com/wiki/Common_Gotchas_In_Python
* https://stackoverflow.com/questions/530530/python-2-x-gotchas-and-landmines
* https://stackoverflow.com/questions/1011431/common-pitfalls-in-python
* https://www.python.org/doc/humor/
* https://github.com/cosmologicon/pywat#the-undocumented-converse-implication-operator
* https://www.codementor.io/satwikkansal/python-practices-for-efficient-code-performance-memory-and-usability-aze6oiq65
* https://github.com/wemake-services/wemake-python-styleguide/search?q=wtfpython&type=Issues
* Обсуждение WFTPython на [Hacker News](https://news.ycombinator.com/item?id=21862073) и на [Reddit](https://www.reddit.com/r/programming/comments/edsh3q/what_the_fck_python_30_exploring_and/).

# 🎓 Лицензия

[![WTFPL 2.0][license-image]][license-url]

&copy; [Satwik Kansal](https://satwikkansal.xyz)

[license-url]: http://www.wtfpl.net
[license-image]: https://img.shields.io/badge/License-WTFPL%202.0-lightgrey.svg?style=flat-square

## Удиви друзей!

Если тебе понравился wtfpython, то ты можешь использовать ссылки ниже, чтобы поделиться с друзьями.

[Twitter](https://twitter.com/intent/tweet?url=https://github.com/satwikkansal/wtfpython&text=If%20you%20really%20think%20you%20know%20Python,%20think%20once%20more!%20Check%20out%20wtfpython&hashtags=python,wtfpython) | [Linkedin](https://www.linkedin.com/shareArticle?url=https://github.com/satwikkansal&title=What%20the%20f*ck%20Python!&summary=If%20you%20really%20thing%20you%20know%20Python,%20think%20once%20more!) | [Facebook](https://www.facebook.com/dialog/share?app_id=536779657179021&display=page&href=https%3A%2F%2Fgithub.com%2Fsatwikkansal%2Fwtfpython&quote=If%20you%20really%20think%20you%20know%20Python%2C%20think%20once%20more!)  

## Нужна pdf версия?

Я получил несколько просьб о pdf и epub версии wtfpython. Вы можете добавить свои контакты [тут](https://satwikkansal.xyz/wtfpython-pdf/) чтобы получить pdf и epub как только они будут готовы.


**На этом всё, ребята!** Чтобы получать информацию о новом похожем контенте, вы можете оставить свой email [здесь](https://www.satwikkansal.xyz/content-like-wtfpython/).
*PS: А ещё можно пожертвовать доллар на [посадку дерева](https://teamtrees.org/).*

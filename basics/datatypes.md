# DataTypes

## Datatypes

```text
graph TD
    Main(DataTypes) --> B(Single Valued DT)
    Main(DataTypes) --> C(Collection DT)
    B(Single Valued DT) --> D(Numeric DT)
    B(Single Valued DT) --> E(Boolean DT)
    E(Boolean DT) --> F(True/False)
    D(Numeric DT) --> G(Integer)
    D(Numeric DT) --> H(Float)
    D(Numeric DT) --> I(Complex)
    C(Collection DT) --> J(String)
    C(Collection DT) --> K(List)
    C(Collection DT) --> L(Tuple)
    C(Collection DT) --> M(Set)
    C(Collection DT) --> N(Dictionary)
```

> #### _**How to check DataType of a variable?**_
>
> Type function helps us to check the datatype of the variable.
>
> Syntax: type\(var\)

```python
>>> a = 1
>>> a
1
>>> type(a)
<class 'int'>
```

#### Integer

Integer datatype stores all kinds of numbers. Irrespective of range or any limitations. Ex:

```python
>>> a = 1
>>> a
1
>>> type(a)
<class 'int'>

# can be of any size
>>> b = 20000000000
>>> b
20000000000

# negative of any size
>>> a = -2000000000
>>> a
-2000000000
>>>
```

#### Float

Float datatype stores any decimal number. Ex:

```python
>>> f = 2.5
>>> f
2.5
>>> type(f)
<class 'float'>

>>> f = 3.141592653589793
>>> f
3.141592653589793
```

#### Complex

Complex DT stores complex numbers in the format of: real part + imaginary part

Ex:

```python
>>> c = 1+0j
>>> c
(1+0j)
>>> type(c)
<class 'complex'>

>>> c = 2 + 5j
>>> c
(2+5j)
```

## Collection Datatypes

Collection datatypes store its items in individual memory blocks. Collection datatypes memory diagram: s = 'hello'

| 0 | 1 | 2 | 3 | 4 |
| :--- | :--- | :--- | :--- | :--- |
| h | e | l | l | o |

li = \[1,2,3,4\]

| 0 | 1 | 2 | 3 |
| :--- | :--- | :--- | :--- |
| 1 | 2 | 3 | 4 |

Single Valued datatypes memory digram: a = 1

| a |
| :--- |
| 1 |

b = True

| b |
| :--- |
| True |

### String

Anything can be stored in a string. Like letters, words, sentences, numbers, symbols, unicode, etc. As long as there are same quotes at the start and end.

* indexing is possible
* string is Immutable, cannot be modified.

> Syntax: var = 'value' var = "value" var = '''value'''

```python
>>> s = 'hello'
>>> s
'hello'
>>> type(s)
<class 'str'>

# sentences
>>> s = 'hello world'
>>> s
'hello world'

# string with letters,symbols,numbers
>>> mail = 'ram420@gmail.com'
>>> mail
'ram420@gmail.com'

# single letters
>>> s = 'A'
>>> s
'A'

# numbers with quotes
>>> s = '200'
>>> s
'200'
>>> type(s)
<class 'str'>

# string with multiple quotes
>>> s = "Bangalore's Best Chicken"
>>> s
"Bangalore's Best Chicken"
>>> 

# string with triple quote which is used mostly for multiline strings.
>>> s = '''Multiline string
with many lines and all kinds of quotes.
"Bangalore's Best Chicken"
and sentences
'''
>>> print(s)
Multiline string
with many lines
and all kinds of quotes.
"Bangalore's Best Chicken"
and sentences
```

s = 'hello'

| 0 | 1 | 2 | 3 | 4 |
| :--- | :--- | :--- | :--- | :--- |
| h | e | l | l | o |

```python
# Indexing is possible
>>> s = 'hello'
>>> s[0]
'h'
>>> s[1]
'e'
>>> s[4]
'o'

# string with quotes
>>> s = "abc's"
>>> s[3]
"'"
>>> s[4]
's'
>>> s[2]
'c'

# string with space
>>> s = 'hi abc'
>>> s[2]
' '
>>> s[3]
'a'

# when invalid index is given, we get IndexError.
>>> s = 'hello'
>>> s[6]
Traceback (most recent call last):
  File "<pyshell#104>", line 1, in <module>
    s[6]
IndexError: string index out of range

# String is Immutable (cannot be modified)
>>> s = 'jello'
>>> s[0] = 'h'
Traceback (most recent call last):
  File "<pyshell#151>", line 1, in <module>
    s[0] = 'h'
TypeError: 'str' object does not support item assignment
```

### List

List stores all kinds of DT's inside it, in the form of a list with each value seperated by a comma.

* indexing is possible
* list is mutable

> Syntax: var = \[value,value2,...\]

```python
>>> li = [1,2,3,4]
>>> li
[1, 2, 3, 4]
>>> type(li)
<class 'list'>

# list with different datatypes
>>> li = [1,2.5,'hello']
>>> li
[1, 2.5, 'hello']
>>> type(li)
<class 'list'>

# list can be indexed
>>> li = [1,2,3]
>>> li[0]
1
>>> li[1]
2

# list is mutable
>>> li = [1,2,3]
>>> li[0] = 200
>>> li
[200, 2, 3]
>>> 
>>> li[1] = 300
>>> li
[200, 300, 3]
```

### Tuple

Tuple datatype is similar to list, except it's immutable.

* Cannot modify elements in a tuple

> Syntax: var = \(value,valu2\)

```python
>>> tu = (1,2,3)
>>> tu
(1, 2, 3)
>>> type(tu)
<class 'tuple'>

>>> tu = (1,2.5,'hello')
>>> tu
(1, 2.5, 'hello')

# Indexing is possible
>>> tu = (1,2,3)
>>> tu[0]
1

# tuples are immutable datatypes
>>> tu[0] = 200
Traceback (most recent call last):
  File "<pyshell#2>", line 1, in <module>
    tu[0] = 200
TypeError: 'tuple' object does not support item assignment
```

### Set

* Does not store repeated items.
* Items are stored in shuffled order.
* Since items are stored in random order and items are not repeated, we cannot index set.
* Cannot modify elements present in a set.\(using indexing\)

> Syntax: var = {value,value1}

```python
>>> se = {1,2,3}
>>> se
{1, 2, 3}
>>> type(se)
<class 'set'>

# set with different DT
>>> se = {1,2.5,'hello'}
>>> se
{1, 2.5, 'hello'}

# set with repeated elements
>>> se = {1,2,1,1,3,4}
>>> se
{1, 2, 3, 4}

# set stores items in random order
>>> se = {7,3,2,6,4}
>>> se
{2, 3, 4, 6, 7}

# indexing is not possible
>>> se = {1, 2, 3, 4}
>>> s[0]
Traceback (most recent call last):
File "<pyshell#25>", line 1, in <module>
    s[0]
TypeError: 'set' object is not subscriptable

# set cannot be modified using indexing BUT >>
>>> s[0] = 20
Traceback (most recent call last):
  File "<pyshell#4>", line 1, in <module>
    se[0] = 2
TypeError: 'set' object does not support item assignment

# set can be modified using inuild function
>>> se = {1,2,3}
>>> se.add(4)
>>> se
{1, 2, 3, 4}
>>> se.remove(1)
>>> se
{2, 3, 4}
```

### Dictionary

* stores data in a key value pair
* keys cannot be repeated
* values can be of any DT

> Syntax var = {key:value,key1:val1,..}

Memory digram of a dictionary: di = {'a':1,'a':2,'b':3}

| K | V |
| :--- | :--- |
| a | 1 |
| b | 2 |
| c | 3 |

```python
>>> di = {'a':1,'b':2,'c':3}
>>> di
{'a': 1, 'b': 2, 'c': 3}
>>> type(di)
<class 'dict'>

# anything can be stored as value
>>> di = {'int':200,'float':2.5,'string':'hello'}
>>> di
{'int': 200, 'float': 2.5, 'string': 'hello'}
>>> type(di)
<class 'dict'>

>>> di = {'name':'ram','id':223}
>>> di
{'name': 'ram', 'id': 223}

# keys cannot be repeated
>>> di = {'a':1,'a':2,'b':3}
>>> di
{'a': 2, 'b': 3}


# Indexing using keys is possible
>>> di
{'a': 1, 'b': 2, 'c': 3}
>>> di['a']
1
>>> di['b']
2

# Modifying values using key is possible
>>> di['a'] = 200
>>> di
{'a': 200, 'b': 2, 'c': 3}
>>> di['b'] = 300
>>> di
{'a': 200, 'b': 300, 'c': 3}

# We can extract only keys/values by using inbuilt 
# functions available in a dictionary
>>> di
{'a': 1, 'b': 2, 'c': 3}
>>> di.values()
dict_values([1, 2, 3])
>>> di.keys()
dict_keys(['a', 'b', 'c'])

# but the datatype is different so we need to typecast it to list.
>>> list(di.values())
[1, 2, 3]
>>> list(di.keys())
['a', 'b', 'c']
```

### Indexing and Mutability Table

| DT | Indexing | Mutability |
| :--- | :--- | :--- |
| String | ✅ | ❌ |
| List | ✅ | ✅ |
| Tuple | ✅ | ❌ |
| Set | ❌ | ✅ |
| Dictionary | ✅ | ✅ |

**Note:**

* Dictionary indexing possible using key
* set can be modified using inbuilt functions
* set cannot be indexed because it stores items in random order and items are not repeated


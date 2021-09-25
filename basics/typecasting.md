# Typecasting

Converting from one datatype to another datatype is called as typecasting

> Syntax: destination\_dt\(var\)

Ex:

```python
>>> li = [1,2,3]
>>> tuple(li)
(1, 2, 3)
```

* Below are the variables which I will be using in this document throughout

  ```python
  >>> i = 100
  >>> f = 2.0
  >>> comp = 1+0j
  >>> booly = True
  >>> s = 'hello'
  >>> li = [1,2,3]
  >>> tu = (1,2,3)
  >>> se = {1,2,3}
  >>> di = {'a':1,'b':2,'c':3}
  ```

* All the DT when converted to string just becomes normal string with the everything as it is from the original var like brackets, comma, spaces, etc.Basically adding quotes front and back of the value.
* All DT when converted to boolean will give True. Only under few conditions it will give us False.
* Boolean will give us False only when we give the bool the default value of DT.
* Converting ANY numeric DT to collection DT is not possible and vice versa too.
* String as number can be typecasted to numeric DT.

Typecasting Table

| From/To | Int | Float | Complex | Boolean | String | List | Tuple | Set | Dictionary |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Int | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Float | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Complex | ❌ | ❌ | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Boolean | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Str\(as number\) | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| String | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| List | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Tuple | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Set | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| Dictionary | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

## Numeric Datatype Typecasting

* **Integer to other DT**

```python
>>> int(i)
100
>>> float(i)
100.0
>>> 
>>> complex(i)
(100+0j)

# boolean and string
>>> bool(i)
True
>>> str(i)
'100'

# integer to all other collection DT not possible
>>> list(i)
Traceback (most recent call last):
  File "<pyshell#66>", line 1, in <module>
    list(i)
```

* Float to other DT

```python
>>> f
2.0
>>> int(f)
2
>>> f = 2.5
>>> int(f)
2
>>> float(f)
2.5
>>> complex(f)
(2.5+0j)
>>> bool(f)
True
>>> tuple(f)
Traceback (most recent call last):
  File "<pyshell#100>", line 1, in <module>
    tuple(f)
TypeError: 'float' object is not iterable
```

## Collection

* Converting any collection DT to set will remove duplicate items
* Converting any collection DT to dictionary is not possible.\(other than list and tuple which requires it to follow key value pair\)

### String

* string to list : will make all the characters in the string to items in list
* string to set : will remove duplicate characters from the string.\(note:it will also shuffle\)

```python
>>> s = 'hello'
>>> list(s)
['h', 'e', 'l', 'l', 'o']
>>> tuple(s)
('h', 'e', 'l', 'l', 'o')

# will remove duplicates
>>> set(s)
{'l', 'o', 'h', 'e'}

# to dictinary not possible
>>> dict(s)
Traceback (most recent call last):
  File "<pyshell#195>", line 1, in <module>
    dict(s)
ValueError: dictionary update sequence element #0 has length 1; 2 is required
```

### String as number

* string as number can be typecasted to other datatypes

```python
>>> sn = '100'
>>> int(sn)
100
>>> float(sn)
100.0
>>> complex(sn)
(100+0j)
>>> bool(sn)
True
>>> list(sn)
['1', '0', '0']
>>> tuple(sn)
('1', '0', '0')
>>> set(sn)
{'0', '1'}
```

### List

* list to dictionary is possible by using nested list and key value pairs.

```python
>>> li = [1,2,3]
[1,2,3]
>>> tuple(li)
(1, 2, 3)
>>> set(li)
{1, 2, 3}
>>> dict(li)
Traceback (most recent call last):
  File "<pyshell#260>", line 1, in <module>
    dict(li)
TypeError: cannot convert dictionary update sequence element #0 to a sequence

# list to dictionary
>>> lidi = [['a',1],['b',2],['c',3]]
>>> lidi
[['a', 1], ['b', 2], ['c', 3]]
>>> dict(lidi)
{'a': 1, 'b': 2, 'c': 3}
```

### Tuple

* we can modify tuples by converting to list.\(basically replacing\)

```python
>>> str(tu)
'(1, 2, 3)'
>>> list(tu)
[1, 2, 3]
>>> set(tu)
{1, 2, 3}

>>> tudi = (('a',1),('b',2))
>>> dict(tudi)
{'a': 1, 'b': 2}

# modifying tuple
>>> t
(1, 2, 3)
>>> tl = list(t)
>>> tl[0] = 100
>>> t = tuple(tl)
>>> t
(100, 2, 3)
```

#### Set

* set too like tuple can be converted to other DT inorder to modify it.
* set cannot be converted to dictionary as set inside set is not possible.

```python
>>> se = {1,2,3}
>>> str(se)
'{1, 2, 3}'
>>> list(se)
[1, 2, 3]

# modifying set by converting to list
>>> se = {1,2,3}
>>> seli = list(se)
>>> seli
[1, 2, 3]
>>> seli[0] = 200
>>> seli
[200, 2, 3]
>>> se = set(seli)
>>> se
{200, 2, 3}

# set inside set/set as dict
>>> sedi = {{'a',1},{'b',2}}
Traceback (most recent call last):
  File "<pyshell#109>", line 1, in <module>
    sedi = {{'a',1},{'b',2}}
TypeError: unhashable type: 'set'
```

#### Dictionary

* Converting dictionary to other DT will give us only keys.

```python
>>> di = {'a': 1, 'b': 2, 'c': 3}
>>> str(di)
"{'a': 1, 'b': 2, 'c': 3}"
>>> list(di)
['a', 'b', 'c']
>>> tuple(di)
('a', 'b', 'c')
>>> set(di)
{'c', 'b', 'a'}

# values can also be extracted
# by using dict inbuilt fn
>>> list(di.values())
[1, 2, 3]
>>> list(di.keys())
['a', 'b', 'c']
```


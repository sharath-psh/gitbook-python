# Indexing and Slicing

Topics

* Indexing
  * Positive indexing
  * Negative indexing
  * Errors:
    * Invalid indexes/out of range
    * only integers
    * DT's which can be indexed
* Slicing
  * Positive slicing
  * Negative slicing
  * sentences, words
  * slicing examples &gt; string,list,
  * tuple
  * giving blank index
  * Errors:
    * Invalid indexes/out of range
    * empty return if index wrong
  * Updation/Step
    * Syntax
    * Positive updation
    * Negative updation
    * Reversing coll
    * Errors:
      * 1 as step

### Indexing

Indexing is where we can get an item from collection using the index value of the collection.

Memory diagram of string with index values:

s = 'hello'

| 0 | 1 | 2 | 3 | 4 |
| :--- | :--- | :--- | :--- | :--- |
| h | e | l | l | o |

List : li = \[1,2,3,4\]

| 0 | 1 | 2 | 3 |
| :--- | :--- | :--- | :--- |
| 1 | 2 | 3 | 4 |

Dictionary :

| Key | Value |
| :--- | :--- |
| a | 1 |
| b | 2 |
| c | 3 |

* Indexing always starts with 0.
* Datatypes which can be indexed are : String, List, Tuple.
* len\(var\) helps us to find the length of the collection.

### Positive Indexing

s = 'hello'

| 0 | 1 | 2 | 3 | 4 |
| :--- | :--- | :--- | :--- | :--- |
| h | e | l | l | o |

> Syntax var\[index\]

```python
>>> s = 'hello'
>>> s[0]
'h'
>>> s[1]
'e'

# giving invalid index results in IndexError
>>> s[5]
Traceback (most recent call last):
  File "<pyshell#3>", line 1, in <module>
    s[5]
IndexError: string index out of range

# length function
>>> len(s)
5

# using length function inside indexing giving us the last element
# -1 is done for adjusting with 0 index
>>> s[len(s)-1]
'o'

# indexing list and tuple
>>> li = [1,2,3]
>>> li[0]
1
>>> t = (1,2,3)
>>> t[0]
1
```

### Negative Indexing

s = 'hello'

| -5 | -4 | -3 | -2 | -1 |
| :--- | :--- | :--- | :--- | :--- |
| h | e | l | l | o |

* negative indexing starts with -1
* goes from right to left

```python
>>> s[-1]
'o'
>>> s[-2]
'l'
>>> s[-5]
'h'
```

## Slicing

* Slicing is extracting a part of the collection using indexing.
* remember to do ending index + 1

> Syntax var\[starting index:ending index+1\]

s = 'hello world'

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| h | e | l | l | o |  | w | o | r | l | d |

```python
>>> s = 'hello world'
>>> s[0:5]
'hello'
>>> s[6:11]
'world'

>>> s = 'microphone'
>>> s[:5]
'micro'
>>> s[5:]
'phone'

>>> n = 'notepad'
>>> n[:4]
'note'
>>> n[4:]
'pad'

# slicing a list
>>> li = [1,2,3,4,5,6,7,8,9,10]
>>> # 3 to 7
>>> li[2:7]
[3, 4, 5, 6, 7]

# slcing a tuple
>>> tu = (1,2,3,4,5,6,7,8,9,10)
>>> tu[2:7]
(3, 4, 5, 6, 7)

# negative slicing
s = 'hello'
| -5| -4| -3| -2| -1|
|---|---|---|---|---|
| h | e | l | l | o |
>>> s[-5:-1]
'hell'

# giving invalid indexes will not result in errors
>>> s[111:999]
''
>>> s[-1111:99999]
'hello world'
>>> s[12:22]
''
```

* we can give blank/space/nothing in the place of index, if the index is first or last index of the collection.

> Syntax var\[:EI+1\] var\[SI:\]

```python
>>> s = 'hello world'
>>> s[:5]
'hello'
>>> s[6:]
'world'
>>> s[:]
'hello world'

>>> s = 'dashboard'
>>> s[4:]
'board'
```

### Updation/Step

We can skip or step items in the collection and perform slicing

> Syntax var\[SI:EI+1:step\]

s = 'hello world'

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| h | e | l | l | o |  | w | o | r | l | d |

li = \[1, 2, 3, 4, 5, 6, 7, 8, 9, 10\]

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |

```python
>>> s = 'hello world'
>>> s[::2]
'hlowrd'

>>> li
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# updation as 2
>>> li[::2]
[1, 3, 5, 7, 9]

# using updation to print even numbers in the list
>>> li[1::2]
[2, 4, 6, 8, 10]

# updation can be any number
>>> li[::3]
[1, 4, 7, 10]
>>> li[::4]
[1, 5, 9]

# giving updation of 1 doesnt matter as it will step 1.
>>> li[::1]
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

### Negative updation

* Negative updation is best used to reverse any collection.
* \[::-1\] can be used anywhere throughout python and not just for slicing purposes
* can be chained with other python code to reverse data.

> Syntax var\[::-1\]

```python
>>> s = 'hello'
>>> s[::-1]
'olleh'

>>> li = [1,2,3]
>>> li[::-1]
[3, 2, 1]

# can be chained
>>> s = 'hello world'
>>> s[:5][::-1]
'olleh'
```


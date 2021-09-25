# Generator and Iterator

* Any DT which can be in a for loop, is a iterator.
* Common iterators are list,string,tuple,set,dict,range,file open.

Uses:

1. Memory efficiency: Incase of a long iterable, we can use generators and iterators to go element by element in the iterable.
2. Can go through a infinite stream efficiently.

### iter object presence in any iterable

```python
li = [1,2,3]
print(dir(li))
print(li.__iter__)

# o/p --->
# ['__add__', '__iter__', ....., 'sort']
# <method-wrapper '__iter__' of list object at 0x000001F0DADE5208>
```

### demonstration of iterator

```python
li = [1,2,3]
iobj = iter(li)
print(next(iobj))
print(next(iobj))
print(next(iobj))

# o/p --->
# 1
# 2
# 3
```

### iterate using for loop

```python
li = [1,2,3]
iobj = iter(li)
print(iobj)

for i in li:
    print(next(iobj))

while True:
    try:                
        print(next(iobj))
    except:
        break

# o/p --->
# 1
# 2
# 3
```

### StopIteration Error when we reach the end of the iter obj.

```python
li = [1,2,3]
iobj = iter(li)
print(next(iobj))
print(next(iobj))
print(next(iobj))
print(next(iobj))

# 1
# 2
# 3
# Traceback (most recent call last):
#   File "tracing.py", line 6, in <module>
#     print(next(iobj))
# StopIteration
```

## Generators

* Generators are similar to iterators but in the form of a function.
* We need to create a function which has the statement 'yield' in it.
* a function can have multiple yield statements.
* we need to create a generator object in order to work with such functions.

Syntax:

```python
def fn():
      ----
      yield exp

gen_objn = fn()
var = next(gen_objn)
```

### Generator Examples

```python
# Generator example
def fn():
    yield 1                     # creating 1st yield stmt
    yield 2                     # creating 2nd yield stmt......
    yield 3
    yield 4

gobj = fn()                     # creating the generator obj
print(gobj)
while True:
    try:
        print(next(gobj))
    except:
        break

# o/p
# <generator object fn at 0x000001C02A01BC48>
# 1
# 2
# 3
# 4
```

```python
def mygenerator():
    print('First item')
    yield 10

    print('Second item')
    yield 20

    print('Last item')
    yield 30

iobj = mygenerator()
print(next(iobj))
print(next(iobj))
print(next(iobj))
```

### generator example

```python
li = [1,2,3,4]

lc = [i**2 for i in li]
print(lc)

gen = (i**2 for i in li)
print(next(gen))
print(next(gen))
print(next(gen))
```


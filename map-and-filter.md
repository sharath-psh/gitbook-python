# Map and Filter

map\(\) function applies a given function to each item of an iterable \(list, tuple etc.\) and returns a list of the results.

Syntax:

```text
map(function,iterable/collection)
```

* function to which each of the item of the collection to be passed

```python
def sqr(a):
    return a**2

li = [1,2,3,4]
res = map(sqr,li)
print(res)
cl = list(res)
print(cl)

# o/p
# <map object at 0x0000021AD4E3F848>
# [1, 4, 9, 16]
```

#### Find the length of the items in the list

```python
cl = ['hello', 'how', 'are', 'you']

def fl(x):
    return len(x)

res = map(fl,cl)
print(list(res))
```

#### converting from lower to upper

```python
def ul(s):
    return s.upper()
s = ('php','java','python','c++','c')
res = list(map(ul,s))
print(res)
```

### we can write full functions

```python
def ul(s):
    if s.isupper():
        return s.lower()
    else:
        return s.upper()

s = 'HeLlo'
res = list(map(ul,s))
fs = ''
for i in res:
    fs = fs + i
print(fs)
```

## Filter

#### WAP to print only even numbers from the list

```python
li = list(range(1,21))

def ef(n):
  if n%2==0:
    return n

x = filter(ef,li)
print(list(x))

x = filter(lambda x:x%3==0,li)
```


# List Comprehension

when we want to add items to the list but also do a small logic before adding it to the list.

* list comprehension helps us in appending items to a list with an expression.
* we can basically have a for loop inside a list
* we can avoid writing code to append items individually in the list.

  Syntax:

  var = \[expression for var in coll/iter\]

## Add elements to the list

### Without list comprehension

```python
li = []
for i in range(1,11):
    li.append(i)
print(li)
```

### using list comprehension

```python
li = [i for i in s]
print(li)
```

## Adding items to the list with an expression

```python
li = []
for i in range(1,11):
    li.append(i**2)
print(li)
```

```python
li = [i**2 for i in range(1,11)]
print(li)
```

## Appending letters to a list

```python
s = 'hello'
li = []
for i in s:
    li.append(i)
print(li)
```

```python
li = [i for i in s]
print(li)
```

## list comprehension with if condition

```python
li = [i for i in range(1,11) if i%2== 0]
print(li)
```

```python
# nested if
li = [i for i in range(100) if i%3==0 if i%5==0]
print(li)
```

## Problems

```python
s = 'hello how are you'
li = [i[::-1] for i in s.split()]
print(li)
```

```python
# random numbers in list
import random
li = [random.randint(1,11) for i in range(5)]
print(li)
```

```python
# squares of a list
li = [32,5,5,23,5]
nl = [i**2 for i in li]
print(nl)
```

```python
# names starting with the letter 'h'
s = 'hello how are you'
li = s.split()
```

```python
nl = [i for i in li if i[0]=='h']
print(nl)
```

```python
# if else 
li = [o/p if condition else o/p for loop]
li = ['Even' if i%2==0 else 'Odd' for i in range(10)]
print(li)
```


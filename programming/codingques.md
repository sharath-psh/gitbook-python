# Coding Questions

## Very Easy

- sum of 3 numbers, if all 3 same then return 3 times of it

```python
a,b,c = 3,3,3

sum = a + b + c

if a==b ==c:
    print(sum*3)
else:
    print(sum)
```

---

- Check if list is empty

```python
li1 = []
li2 = [1,2,3]

def check_list(l):
    if len(l)==0:
        print('list empty')
    else:
        print('list not empty')

check_list(li1)
check_list(li2)

# ------------------------

if li:
    print('Empty List')
else:
    print('list not empty')

```

---

- WAP to find the length of the list

```python
li = [1,2,3,4]
print(len(li))
count = 0
for i in li:
    count = count + 1
print(count)
```

---

## Basics

- Count the number of digits in a number

```python

i = 100
count = 0

if i == 0:
    count = 1
else:
    while i != 0:
        i = i//10
        count = count + 1

print(count)

# ----------------------------

n = 100
n = str(n)
count = 0
for i in n:
    count = count + 1
print(count)

# ----------------------------

n = 100
n = str(n)
print(len(n))

```

---

- WAP to find the factorial of given number

```python
n = 5
f = 1
for i in range(1,n+1):
    f = f * i
print(f)

# ---------
# using recurssion
def fact(n):
    if n == 0:
        return 1
    return n * fact(n-1)
print(fact(5))
```

---

- Remove duplicates in a list

```python
li = [1,1,2,3,2,4]
ndl = []
for i in li:
    if i not in ndl:
        ndl.append(i)
print(ndl)
# -----------

print(set(li))
```

---

- WAP to append even and odd numbers in seperate list

```python
li = [1,2,45,7,3,4,7,3]
print(li)
eli,oli = [],[]
for i in li:
    if i%2 == 0:
        eli.append(i)
    else:
        oli.append(i)
print(eli)
print(oli)
```

---

- WAP to count positive and negative numbers in the list

```python
li = [i for i in range(-5,6)]
pcount,ncount = 0,0
for i in li:
    if i>0:
        pcount = pcount + 1
    else:
        ncount = ncount + 1
print(pcount,ncount)
```

---

- WAP to find largest number in a list

```python
import random
li = [random.randint(1,11) for i in range(1,6)]
print(li)
max = li[0]
for i in li:
    if i>max:
        max = i
    else:
        continue
print(max)
```

---

- WAP to find the smallest number in the list

```python
min = li[0]
for i in li:
    if i<min:
        min = i
print(min)
```

---

- WAP to find the 2nd largest in the list

```python
import random
li = [random.randint(1,11) for i in range(1,6)]
print(li)
li = list(set(li))
li.sort()
print(li)
print(li[-2])
```

---

- Combine two lists

```python
l1 = [1,2,3]
l2 = [1,2,3]
lc = []
for i in l2:
    lc.append(i)
for i in l1:
    lc.append(i)
print(lc)
```

---

- Add two lists

```python
l1 = [1,2,3]
l2 = [1,2,3]

def adder(a,b):
    return a+b

sl = list(map(adder,l1,l2))
print(sl)
```

---

- FizzBuzz

```python
for i in range(1,101):
    if i%3 == 0 and i%5 == 0 :
        print('FizzBuzz')
    elif i%3 == 0 :
        print('Fizz')
    elif i%5 == 0:
        print('Buzz')
    else:
        print(i)
```

## Medium

- Collatz Conjecture

```python
n = 20
while n>=2:
    if n%2 == 0:
        n = n/2
        print(n)
    else:
        n = (n*3) + 1
        print(n)


# n = int(input('Enter number'))
def col(f):
    if f<2:
        print('loop ended')
    elif f%2 == 0:
        f = f/2
        print(f)
        col(f)
    else:
        f = (f*3) + 1
        print(f)
        col(f)

col(n)

```

- Count the number occurences of each item in the list

```python
li = [1,1,1,1,1,2,2,2,3,3,3,3,5]
di = {}
count = 0
for i in li:
    if i not in di.keys():
        di[i] = 0
        count = 1
    else:
        count = count + 1
        di[i] = count

print(di)


dc = {i:li.count(i) for i in li}
print(dc)
```

## Advanced Concepts

### List comprehension

- Flatten a multi-dimensional list

```python
my_list = [[10,20,30],[40,50,60],[70,80,90]]
flattened = [x for temp in my_list for x in temp]
# output => [10, 20, 30, 40, 50, 60, 70, 80, 90]
```

---

---

# Mini Projects

```python
from random import shuffle

cl = ['','','1']
shuffle(cl)
print(cl)

guess = int(input('Enter ball location (1,2,3): '))

if guess == cl.index('1')+1:
    print('correct')
else:
    print('wrong')
```

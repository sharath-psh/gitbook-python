# If/Else

#### Control Statements

* Controls the flow of execution using the conditional statements.

2 types of control statements

1. Descional Statements
2. Looping Statements

Under Descional statements we have :

a. Simple if Statements b. If else Statements c. If elif Statements d. Nested if Statements

**If-else statements**

Syntax:

```python
if condition:
    -------
else:
    -------
```

* Here condition can be anything which will give us True or False.
* Statements present inside the if block must be indented with 1 tab space.
* condition example : a&gt;b, a==0, True, 'e' in 'hello', etc.
* else statements do not have any conditions.
* giving a condition in the else statement will result in a error.

Programming Questions :

* WAP to check if the number is 0 or not.

```python
a = 0
if a == 0:
    print('a is zero')
else:
    print('a is not zero')
```

* WAP to check if a number is even or odd.

```python
a = 6
if a%2 == 0:
    print('Even number')
else:
    print('Odd number')
```

* WAP to check if letter 'e' is present in the string 'hello'

```python
s = 'hello'
if 'e' in s:
    print('e is present')
else:
    print('e is not present')
```

* WAP to check whether a or b is greater

```python
a = 3
b = 2

if a>b:
    print('a is greater than b')
else:
    print('b is greater than a')
```

* WAP to check whether the given character is a vowel or not, if not a vowel print 'consonant'

```python
s = 'e'
sv = 'aeiou'
if s in sv:
    print('vowel')
else:
    print('consonant')
```

* WAP to check if a number is a mulitple of 5

```python
a = 10
if a%5 == 0:
    print('its a multiple of 5')
else:
    print('not a multiple')
```

* WAP to check if character is lower case or not

```python
c = 'A'
if c>='a' and c<='z':
    print('lowercase')
else:
    print('not lowercase')
```

* WAP to convert uppercase to lowercase and vice versa

```python
s = 'L'
if s>='a' and s<='z':
    print(chr(ord(s)-32))
else s>='A' and s<='Z':
    print(chr(ord(s)+32))
```

* WAP to check if a number is positive or negative

```python
if a == 0:
    print('a is zero')
elif a>0:
    print('a is positive')
else:
    print('a is negative')
```

* WAP to grade students marks 

  80 - 100 --&gt; A

  60 - 79 --&gt; B

  41 - 59 --&gt; C

   F

* Shipping company

  If parcel is within India and parcel is below Rs.500, then just print cost with shipping charges of Rs.50

  If parcel is within India and parcel is above Rs.500, then just print the cost

  If parcel is outside India, then add shipping chrages of Rs.200

product\_cost = 600 dest = India

```python
pc = 300
dest = 'India'

if dest == 'India':                # checking if dest is india
    if pc>=500:                    # checking if price is greater than 500.
        print('No shipping charges : ', pc)
    else:
        pc = pc + 50               # if price is less than 500, adding shipping cost of 50
        print('Shipping charges add(Rs.50) : ',pc)
else:
    pc = pc + 200                  # since dest is outside india, add shipping cost of 200
    print('Destination outside India, Shipping charges added(Rs.200) : ',pc)
```

* check if 'w' is present in the 3rd place of string 'how'

```python
s = 'how'

if s[2] == 'w':
    print('w is present')
else:
    print('w is not present')
```

* Greatest of 4 numbers

```python
a = 8
b = 6
c = 5
d = 4

if a>b and a>c and a>d:
    print('a is greatest')
elif b>c and b>d:
    print('b is greatest')
elif c>d:
    print('c is greatets')
else:
    print('d is greatest')
```

**If elif**

* WAP to check if greatest number, also check if both a and b are equal

```python
a = 1
b = 1

if a>b:
    print('a is greatest')
elif b>a:
    print('b is greatest')
else:
    print('a and b are equal')
```

* WAP to check if uppercase, or lowercase or its a symbol

```python
s = '@'
if s>='a' and s<='z':
    print('lowercase')
elif s>='A' and s<='Z':
    print('uppercase')
else:
    print('symbol')
```

* WAP to check the greatest of 3 numbers

```python
a = 5
b = 4
c = 3
if a>b and a>c:
    print('a is greatest')
elif b>c:
    print('b is greatest')
else:
    print('c is greatest')
```

**Nested if**

* Program for greatest of 3 numbers in nested if.

```python
a = 5
b = 6
c = 7

if a>b:
    if a>c:
        print('a is greatest')
    else:
        print('c is greater')
else:
    if b>c:
        print('b is greater')
    else:
        print('c is greater')
```

**WAP to check if number is positive or negative using nested if and if/elif**

```python
# --- using nested if
a = -3

if a != 0:
    if a<0:
        print('negative')
    else:
        print('positve')
else:
    print('zero')

# --- using elif

if a == 0:
    print('zero')
elif a>0:
    print('positive')
else:
    print('negative')
```

**While loop**

Syntax :

```python
while condition:
    ----------
    ----------
```

* while block executes the block of code as long as the condition is True
* while can be executed infinitely
* ctrl + c ---&gt;&gt; for stopping a while loop

Comparison of if and while :

```python
if True:
    print('hello')
print('execution completed')
# hello
# execution completed

while True:
    print('hello')
print('execution completed')
# ---> hello hello........
```

* WAP to print numbers from 1 to infinite

```python
n = 1
while True:
    n = n + 1
    print(n)
# 1 2 3 4 5 6 7 ...
```

* WAP to print numbers until 10 using while loop

```python
n = 1       # initializing
while n<11:     # while condition >> here condition checks if n is less than 11
    print(n)
    n = n + 1      #counter
```

* WAP to print even numbers until 10 using while loop

```python
n = 1       # initializing
while n<11:
    if n%2 == 0:
        print(n)
    n = n + 1      #counter

n = 2
while n<11:
    print(n)
    n = n + 2
```

* WAP to print even numbers from 20 to 50

```python
n = 20
while n<51:
    if n%2 == 0:
        print(n)
    n = n + 1
```

* WAP to print A to Z

```python
n = 65     # initializing
while n<91:     # while condition >> here condition checks if n is less than 11
    print(chr(n))
    n = n + 1
```

* WAP to find sum of numbers from 1 to 10

```python
n = 1
while n<11:
    n = n + 1
print(n)
```


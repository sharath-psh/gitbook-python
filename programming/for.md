# For Loops

Syntax :

```python
for var in coll/iterable:
    ---------
    ---------
```

* for loop is used to 'iterate' through a collection.
* once the end of the collection is reached, the for loop exits out and the remaining code is executed
* 'collection' is where we can give any type of collection, i.e list,string,tuple,set,dictionary.
* 'var' is where the items/elements of the collection is stored.
* we use 'i' usually in for loop as the variable.
* there are no conditions in a for loop, its just a looping statment.

Ex:

```python
li = [1,2,3,4]
for i in li:
    print(i)

# O/P
# --->
# 1
# 2
# 3
# 4
```

Examples with other collection datatypes

```python
# list 
>>> li = [2,3,5,6]
>>> for i in li:
 print(i)
2
3
5
6

# string 
>>> s = 'hello'
>>> for i in s:
 print(i)
h
e
l
l
o

# tuple 
>>> tu = (1,2,3,4)
>>> for i in tu:
 print(i)
1
2
3
4

# set
>>> se = {1,2,3,4}
>>> for i in se:
 print(i)


1
2
3
4

# dictionary >>Only keys are printed<<
# dictionary for loop to print keys
>>> di = {'a': 1, 'b': 2, 'c': 3}
>>> for i in di:
 print(i)
a
b
c

# how to print values of the dictionary?
# we are able to print values using the 
# syntax : var[key]
>>> di
{'a': 1, 'b': 2, 'c': 3}
>>> di['a']
1
>>> di['b']
2
>>> di['c']
3

# since dict for loop prints keys
>>> for i in di:
 print(i)
a
b
c

# dict for loop to print values
# we are able to insert our keys in the 
# place of the dictionary
>>> for i in di:
 print(di[i])


1
2
3
>>> # di[i] in the place of 'i' keys are stored
>>> # therefore we are following the syntax to get the values of the dictionary
>>> # dict_name[key]
```

#### WAP to print 'l is here' whenever there is 'l' in the given string

```python
s = 'hello'
for i in s:      # iterating through the string
 if i == 'a':    # checking if the element in the string is 'a'
  print('a is here')  # print 'a is here' when the condition is true


# --->
# a is here
# a is here
```

**WAP to print if number 2 is present in the list**

```python
li = [1,3,3,4]

for i in li:
    if i == 2:
        print('2 is present')
# --->
# 2 is present
```

**WAP to print even and odd numbers in the list**

```python
li = [1,2,3,4,5,6]

for i in li:
    if i % 2 == 0:
        print(i,' is even')
    else:
        print(i,' is odd') 

# --->
# '1 is odd'
# '2 is even'
# '3 is odd'
# ....
```

#### WAP to print vowels present in the string

```python
s = 'hello'
for i in s:
 if i in 'aeiou':
  print(i,'is a vowel')

# --->
# e is a vowel
# o is a vowel
```

**WAP to print consonants and then print the count of consonants**

```python
s = 'hello'
counter = 0
for i in s:
 if i not in 'aeiou':
  print(i,'is a consonant')
  counter = counter + 1
print('count of consonants is : ' + str(counter))

# --->
# h is a consonant
# l is a consonant
# l is a consonant
# count of consonants is : 3
```

#### How to concatinate string using for loop

```python
s = 'hello'
for i in s:
    print(i)
h
e
l
l
o
```

* we are just print the letter of the string individually

  for loop with concatinating the letters to a final string

```python
fs = ''
s = 'hello'
for i in s:
    fs = fs + i

print(fs)
# hello
```

#### WAP to convert string letters from uppercase to lowercase and vice verse

s = 'HeLlo WoRLd' o/p ---&gt; 'hElLO wOrlD'

```python
s = 'HeLlo WoRLd'
fs = ''
for i in s:
    if i == ' ':
        fs = fs + i       # fs here is concatinating if there is a space
    elif i>='a' and i<='z':     # checking if 'i' is small letter
        fs = fs + chr(ord(i)-32)   # converting small to capital using ascii and then concainating to the fs
    else:
        fs = fs + chr(ord(i)+32)

print(fs)
```

#### WAP to find sum of numbers from 0 to 10

```python
sum = 0       # sum initilized with 0
i = 0       # initilizer 'i' starts with 0
while i<=10:     # while loop until 10
 sum = sum + i
 #sum = 0 + 1    # adding the new number to the existing number
 i = i + 1
 #i = 0 + 1     # incrementing the number 'i'
print(sum)

res = 0
for i in range(11):
 res = res + i
print(res)
```

#### WAP to print even numbers from 10 to 20

```python
for i in range(10,21):
    if i%2 == 0:
        print(i)
```

#### WAP to print even numbers from 30 to 50

```python
for i in range(30,51):
     if i%2 == 0:
      print(i)
```

## Nested for loop

```python
li = ['hello','python']

for i in li:
 for j in i:
  print(j)

# O/P
# --->
# h
# e
# l
# l
# ......
```

#### WAP to generate names based on the list of first names and last names

```python
fname = ['ram','sunitha','santosh','sanjay','sunil']
lname = ['chopra','gowda','jain','kumar','kapoor']

for i in fname:
    for j in lname:
        print(i , j)

# o/p -->
# ram chopra
# ram gowda
# ram jain
# ram kumar
# ram kapoor
# sunitha chopra
# sunitha gowda
# sunitha jain
# sunitha kumar
# sunitha kapoor
# santosh chopra
# santosh gowda
# santosh jain
# santosh kuma
```

#### WAP to print the vowels present in the list

```python
li = ['hello','how','are']

for i in li:
 for j in i:
  if j in 'aeiou':
   print(j)
```

```python
>>> s = 'hello'
>>> for i in range(5):
 print(i)


0
1
2
3
4
>>> #when u do range(5) it starts from 0 which looks exactly how our collection indexing looks
>>> s = 'python hello'
>>> s = 'python'
>>> len(s)
6
>>> for i in range(len(s)):
 print(i)


0
1
2
3
4
5
>>> s[0]
'p'
>>> s[1]
'y'
>>> s[2]
't'
>>> s[3]
'h'
>>> s[4]
'o'
>>> s[5]
'n'
>>> s[6]
Traceback (most recent call last):
  File "<pyshell#17>", line 1, in <module>
    s[6]
IndexError: string index out of range
>>> for i in range(len(s)):
 print(s[i])


p
y
t
h
o
n
>>> for i in range(len(s)):
 print(0,s[i])


0 p
0 y
0 t
0 h
0 o
0 n
>>> for i in range(len(s)):
 print(i,s[i])


0 p
1 y
2 t
3 h
4 o
5 n
>>>
```

**WAP to print the index of vowels in the string**

```python
s = 'hello'
for i in range(len(s)):
 if s[i] in 'aeiou':
  print('vowel : ', s[i], ' index at : ', i)
```

* len\(s\) &gt;&gt; 6 &gt;&gt; getting the length of string

  range\(len\(s\)\) &gt;&gt; range\(6\) &gt;&gt; 0,1,2....5 &gt;&gt; using the length of string to generate range function numbers

* i &gt;&gt; 0 &gt;&gt; which is the generated numbers from the range function
* s\[i\] &gt;&gt; s\[0\] &gt;&gt;&gt; we are printing the letter using indexing

#### WAP to print the indexes of a string present inside a list

```python
li = ['hello', 'world']
for i in li:                                # iterating through list    i --> 'hello' li --> ['hello,'world']
    for j in range(len(i)):                 # iterating through string  j --> 0,1,2,... i ---> 'hello'
        print('letter:',i[j],'index',j)     # i[j] --> 'hello'[0]    j --> 0,1,2....


# o/p --->
# h 0
# e 1
# l 2
# l 3
# o 4
# w 0
# o 1
# r 2
# l 3
# d 4
```

**WAP to print the vowels present in the string, which is present inside the list**

```python
lis = ['hello','python']
for i in lis:                         # i contains the elements of the list; i.e:'hello'
 for j in i:                         # j contains the elements of the string; i.e: 'h'
  if j in 'aeiou':                # check if j (letters) are vowels
   print('vowel :' + j)        # printing j (letters)


for i in lis:                           # i contains the words in the list
    for j in range(len(i)):             # j contains 0,1,2,3... || range(len(i)) >> range(len('hello'))
            if i[j] in 'aeiou':         # i[j] >>> 'hello'[0]
      print('vowel :' + i[j] + ' index : ' + str(j))      #i[j] >> hello[0] || j >> 0

# o/p
# vowel :e index : 1
# vowel :o index : 4
# vowel :o index : 4
```

### break statement

* break is used to stop the execution of the current loop

Ex:

```python
li = [1,2,3,4,5]
for i in li:
 if i == 3:
  break
 else:
  print(i)

# o/p
# --->
# 1 2 3
```

### continue

* continue will proceed onto to the next iteration without doing anything

```python
li = [1,2,3,4,5]
for i in li:
 if i == 3:
  continue
 else:
  print(i)

# o/p
# --->
# 1 2 4 5
```

#### WAP to print only the username of the email id

```python
s = 'python@gmail.com'
s = 'abc@gmail.com'
 o/p --> 'abc' 'python'
fs = ''
for i in s:     # since username is present till '@' 
 if i == '@':   # we are gonna iterate until we find '@'
  break    # once we find '@' we are gonna exit out using the break statement
 else:
  fs = fs + i   # i is the characters from the strin
print(fs)     # fs(final string) is the concatination of all the characters until '@'
```

#### Print the mail ids from the list

```python
fs = ''
li = ['ram@gmail.com', 'samuel@gmail.com']
for mails in li:
    for i in mails:
        if i == '@':
            break
        else:
            fs = fs + i
    print(fs)               # printing fs before clearing and moving to next element
    fs = ''                 # clearing fs before moving to next element
```

#### FizzBuzz

1. if the number is a multiple of 3 then print Fizz
2. if the number is a multiple of 5 then print Buzz
3. if it is a multiple of both 3 and 5 then print FizzBuzz

```python
for i in range(1,31):
    if i%3 == 0 and i%5 == 0:
        print('FizzBuzz')
    elif i%3 == 0:
        print('Fizz')
    elif i%5 == 0:
        print('Buzz')
    else:
        print(i)

# # o/p
# 1
# 2
# Fizz
# 4
# Buzz
# Fizz
# 7
# 8
# Fizz
# Buzz
# 11
# Fizz
# 13
# 14
# FizzBuzz
# 16
# 17
# 18
# Fizz
# Buzz
```

#### WAP to count even and odd numbers in the range.

```python
for i in range(500,1000):
    if i%2==0:
        eCount += 1
    else:
        oCount += 1
print(eCount)
print(oCount)
```

#### WAP to print numbers range in reverse order.

```python
for i in range(1,10)[::-1]:
    print(i)
```

#### Write a Python program to construct the following pattern, using a nested loop number. Go to the editor

Expected Output:

1 22 333 4444 55555 666666 7777777 88888888 999999999

```python
for i in range(10):
    print(str(i)*i)
```

**Write a Python program to create the multiplication table \(from 1 to 10\) of a number. Go to the editor**

Expected Output:

Input a number: 6  
6 x 1 = 6  
6 x 2 = 12  
6 x 3 = 18  
6 x 4 = 24  
6 x 5 = 30  
6 x 6 = 36  
6 x 7 = 42  
6 x 8 = 48  
6 x 9 = 54  
6 x 10 = 60


# Functions

* Set of instructions which we can call multiple times,
* Functions help us to reduce repeated code,and also save memory.

Syntax:

```python
def function_name():            
    ---------------
    --Statements---
    ---------------
function_name()
```

Note : return and args are not necessary

Ex: Simple function which prints 'hello'

```python
def sh():               # creating a simple function 'sh'
    print('Hello')      # printing 'hello' statement present inside function
sh()                    # calling function 'sh'
O/P:
'Hello'
```

#### Note : Do not call function before definition

```python
fn()

def fn():
    print('hello')
```

* Defining/creating the function is first, then only we can call the function

#### Mainspace/Global variable

```python
a = 1               # variable 'a' in the main area
def fn():           # creating a simple function 'fn'
    print(a)        # accessing the mainspace var 'a' and printing it
fn()                # calling the function 'fn()'
# --->1

>>Example 2

a = 1
b = 2
def sum():
    sum = a + b
    print(sum)
sum()
# ---> 3
```

* There are two spaces/memory in a function program, mainspace and functionspace.

  The statements present inside the function are executed in the functionspace and

  the statements present in the main area are executed in the mainspace.

* While in the function area if the var we are accessing is not present in the

  function area, it is going to access the var present in the mainspace.

### Function area variable \(local\)

```python
a = 1                       # mainspace var a = 1
def fn():               
    a = 2                   # local/function var a = 2
    print(a)                # accessing the local area var 'a' 2
fn()

# ---> 
# 2             # printing FA var
```

* if the function area has var present inside  the FA, then it is

  given higher preference over MA var

#### Function area var and Mainspace var

```python
a = 1               
def fn():    
    a = 2       
    print(a)        
fn()
print(a)
```

* Function area variable CANNOT modify mainspace variables
* Mainspace CANNOT access function area variables

### To create an empty function

```python
def fn():
    pass
fn()
```

* Function does not get executed until we call the function

```python
def fn():
    ;;error code;;;
    print('hello')
# ---> no output
```

### Function area var destroyed

```python
def fn():
    a = 1
fn()
print(a)
```

* Function data is destroyed once the function is executed.

## Global keyword

### To modify the mainspace variables

```python
a = 1
def fn():
    global a                # global keyword
    a = 2
    print('a present inside the function :',a)

print('printing a before calling the function',a)
fn()
print('printing a after calling the function',a)

# o/p
# --->
# 122
```

* global keyword is used to access and modify the mainspace variables
* when we use 'global' keyword modifying mainspace variables inside the function will modify the

  mainspace variables too.

* global is not recommended to use bcos it will modify the mainspace variables too.
* this will cause the entire python file variables to lose their values.

Syntax:

```python
fn():
    global var,var1
```

## 'return' statement

* To send the function variables to the mainspace

```python
def fn():
    a = 1
a = fn()    # return var is getting stored in var 'a' in the MA
print(a)
# o/p  ---> 1
```

* return statement helps us to send local var back to global.
* to send local var we use the keyword 'return var'
* return statement MUST be in the last line of the function
* return statement can return var,value,expressions
* we need to store returned var in the global using a var or directly

  print it using the print statement, by having the function inside print stmt.

### Arguments /args

```python
a = 1
def fn(a):
    print(a)
fn(a)
```

* arguments are values, or variables which u can send inside the function.
* Formal arguments &gt; arguments present in the function definition.
* Actual arguments &gt; arguments present in the function calling.

```python
Syntax:
def function_name(args):    << formal arg
    ---------
    ---------
function_name(args)         << actual arg
```

* Actual arg missing

```python
a = 1
def fn(a):
    print(a)
fn()        # missing actual arg
```

Error: if we do not pass the actual argument while calling the function, we get the error: Ex : fn\(\) TypeError: fn\(\) missing 1 required positional argument: 'a'

* Formal arg missing

```python
a = 1
def fn():
    print(a)
fn(a)
```

Error: if we do have a formal argument but we are passing actual arg, we get the error: Ex: def fn\(\) TypeError: fn\(\) takes 0 positional arguments but 1 was given

### Multiple arguments

```python
def fn(a,b):
    print('a is :',a)
    print('b is :',b)

fn(1,2)

# o/p --->
# a is : 1
# b is : 2
```

* Position of arguments is important.
* 1st position of the actual arg, goes to the 1st formal arg
* 2nd position of the actual arg, goes to the 2nd formal arg

### Default arguments

```python
Syntax:
def fn(var = value):
    ---stmt--
fn(optional_arg)
```

Example:

```python
def greetings(name = 'Guest'):
    print('Welcome, ',name)

greetings('ram')
greetings()

# o/p --->
# Welcome,  ram
# Welcome,  Guest
```

### Variable arguments / vargs / \*args

Syntax:

```python
def fn(*args):
    print(args)            #  accessing the args
```

```python
def fn(*args):
    print(args)
fn()
fn(1)
fn(3,2)
fn(2,4,6)

# o/p --->
# ()
# (1,)
# (3, 2)
# (2, 4, 6)
```

* args should be the last argument in a function
* we need to use a '\*' in order to use vargs
* it is a industry standard to use 'args' keyword, but anything can be used as var vname
* since args is a tuple, u can access its data as a normal tuple.

### KeyWordArguments / kwargs / \*\*kwargs

```python
def fn(**kwargs):
    print(kwargs)

fn(a=1,b=2,c=3)
fn(name='ram',id=12)

# o/p
# {'a': 1, 'b': 2, 'c': 3}
# {'name': 'ram', 'id': 12}
```

Syntax:

```python
wwdef fn(**kwargs):
    print(kwargs)
fn(key=value,key1=value1)
```

* similar to args,we can send multiple actual args which gets stored in

  the format of tuple in args.

* but in the case of keyword arguments, we send the actual arguments in

  the form of 'key,value' pairs.

* when we send the kwargs in the specified syntax, it gets stored inside a dictionary.
* it is a industry standard to use 'kwargs' keyword, but anything can be used as var vname

### Packing Unpacking

```python
# Packing
def fn(*args):
    print(args)
fn(1,2,3)
# o/p --->
# (1,2,3)

def fn():
    a,b,c = 1,2,3
    return a,b,c
print(fn())
# o/p --->
# (1,2,3)

# ==========================
# Unpacking
def fn(*args):
    print(args)
    print(type(args))
    # unpacking
    for i in args:
        print(i)
fn(1,2,3)

# o/p --->
# (1, 2, 3)
# <class 'tuple'>
# 1
# 2
# 3

def fn():
    a,b,c = 1,2,3
    return a,b,c
tu = fn()
print(tu)
print(type(tu))
for i in tu:
    print(i)

# o/p --->
# (1, 2, 3)
# <class 'tuple'>
# 1
# 2
# 3

# Alternative Unpacking
li = [1,2]
def fn(a,b):
    print(a,b)
fn(*li)
```

### Calculator program

```python
def calc(fn,sn,op):
    fn = int(fn)
    sn = int(sn)
    if op == '+':
        return fn + sn 
    elif op == '-':
        return fn - sn 
    elif op == '*':
        return fn * sn 
    elif op == '/':
        return fn / sn

ui = input('Enter :')
vals = ui.split()
print(calc(vals[0],vals[2],vals[1]))
```

### Program to create list like inbuilt function

```python
li = []
def adder(x):
    if x not in li:
        li.append(x)
        print(x,'added')
    else:
        print(x,'present!')
def remover(x):
    li.remove(x)
    print(x,'removed')

adder(2)
adder(4)
remover(2)
print(li)
```


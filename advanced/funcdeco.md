# Function Decorators

Helps us to execute a set of statements before and after execution of a function.

### Functions can be passed as arguments

```python
def shout(text):
    return text.upper()

def whisper(text):
    return text.lower()

def greet(func):
    greeting = func("Hello World")
    print (greeting)

greet(shout)
greet(whisper)
```

### Python program to illustrate functions can return another function

```python
def outer():
    def inner():
        print("Hello")
    return inner

new = outer()
new()
```

Syntax:

```python
def decorator_fn(normal_fn):
    def inner_fn():
        ---pre task stmts----
        normal_fn()
        ---post task stmts---
    return inner_fn

@decorator_fn
def normal_fn():
    --------
    --------
normal_fn()
```

* Function decorators are used to executed a set of instruction before and after execution of a function.
* We connect a normal function to a decorator function using the annotation along with the function name.
* In the decorator function we follow the specified syntax.
* Inside the inner function of the decorator, we need to specify the statements to be executed before and after the execution of the function.
* func is the standard keyword which we use for the argument.
* inner\(\) is also the standard function name we use to create a function inside function in decorators

## Simple Function decorator

```python
def fd(func):
    def inner():
        print('Stmt before fn execution')
        func()
        print('Stmt after fn execution')
    return inner

@fd
def fn():
    print('fn() being executed')
fn()
```

## Time calculation execution

```python
import time
def time_calc(func):
    def inner():
        st = time.time()
        func()
        et = time.time()
        tt = et - st
        print(tt)
    return inner

@time_calc    
def sum():
    total = 0
    for i in range(1,100000):
        total = total * i
sum()
```


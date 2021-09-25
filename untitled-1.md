# Exception Handling

Exception handling is used when we want to handle an error in the specified block of code.

## Simple exceptional handling example:

```python
a = 1
b = 0
try:
    div = a/b
    print(div)
except:
    print('Exception block executing....')
    print('Division error')
```

* Used to handle the block of code which may contain errors.
* Try block code will execute sucessfully completely when there are no errors in the try block.
* Except block will execute only when there is error in the try block.
* we can have multiple except statements

Syntax:

```python
try:
    ------------
    ------------
except:
    ------------
    executed when error occurs
    ------------
```

Types of except blocks:

1. Specific
2. Generic
3. Default

Common Exception Errors:AttributeError, EOFError, TypeError, ValueError,IndexError, ZeroDivisionError, KeyError

## Specific Exception

```python
a = 1
b = 'aa'
try:
    div = a/b
    print(div)
except ZeroDivisionError:
    print('Exception block executing....')
    print('Variable is Zero')
except TypeError:
    print('Incorrect usage of Datatypes')
```

* Executes except block only when the specified error occurs.

Syntax:

```python
try:
    -------
    -------
except name_of_exception:
    -------
    -------
```

## Generic Exception

```python
a = 1
b = 0
try:
    div = a/b
    print(div)
except ZeroDivisionError:
    print('Cannot be divided by zero')
except Exception:
    print('Exception block executing....')
```

* Used for all exceptions except 'oserror,KeyboardInterrupt'
* Make sure the specified error is above than the generic exception

Syntax:

```python
try:
    ------

    ------

except Exception:
    -------
```

## Diff bw generic except and default Exception

```python
try:
    for i in range(1,100000):
        print(i)
except:
    print('Exception block executing....')
# -------------------------------------------
try:
    for i in range(1,100000):
        print(i)
except Exception:
    print('Exception block executing....')
```

## Default exception

* executes on all exception condition.
* default except statement must be in the last

Syntax:

```python
try:
    ------
except:
    ------
```

## Example of string Indexing

```python
s = input('Enter string: ')
ind = int(input('Enter index u want to fetch: '))

try:
    print(s[ind])
except IndexError:
    print('Invalid Index')
except:
    print('Invalid Index')
else:
    print('ALL OK')
```

## Finally Block

```python
a = 10
b = 5
try:
    div = a/b
    print(div)
except:
    print('Exception Handled...')
finally:
    print('ALL OK')
```

* finally block is optional block.
* Whether try block is executed or except block is executed.
* This block is executed no matter what.
* except is optional when a finally block is present.

Syntax:

```python
try:
    ------
except:
    ------
finally:
    ------
```

## Raise statement

```python
for i in range(1,100):
    if i == 30:
        raise IndexError
    else:
        print(i)
```

* executes the specified error when the given condition occurs.

  Syntax:

  raise name\_of\_exception

## Create our own Exception

```python
class RangeError(Exception):
    pass

for i in range(1,100):
    if i == 30:
        raise RangeError('Range stopping at 30')
    else:
        print(i)
```

creating our own custom exception using raise.

Syntax:

```python
class custom_error_name(Exception):
    pass


raise custom_error_name('Optional Text to describe the error')
```


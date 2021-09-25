# Lambda / Anonymous Function

Syntax:

```text
lambda arguments:expression
```

* can have any number of arguments, but only 1 expression
* cannot have return statements

```python
sqr = lambda x:x*2
print(sqr(5))

# o/p -->
# 10
```

## using lambda and map

```python
li = [1,2,3,4,5,6]
nl = map(lambda x:x**2, li)
print(nl)
print(list(nl))
```

## Write a lambda function to get the last name of the given name

```python
>>> last = lambda n:n.split()[-1]
>>> last('Raj Kumar')
'Kumar'
>>> last('Narendra Damodardas Modi')
'Modi'
```


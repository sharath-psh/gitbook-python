# Access Specifiers

* In OOPs we can control the access of class resources by public and private.

1.Public

* All of the data can be accessed outside the class.
* All the data in python are public by default.

2.Protected

* Programmer convention, to warn devs not to access or modify the var unless it's a sub class.

  [https://docs.python.org/3.3/tutorial/classes.html\#private-variables](https://docs.python.org/3.3/tutorial/classes.html#private-variables)

3.Private

* Class members cannot be accessed outside its own class.

## Private data

```python
class A:
    __a = 1
def__fn():
        print('hello')

print(A.__a)
A.__fn()

# o/p --->
# Traceback (most recent call last)
# File "tracing.py", line 6, in <module>
# print(A.__a)
# AttributeError: type object 'A' has no attribute '__a'
```

### Accessing private data

```python
class A:
    __a = 1
    def__fn():
        print('hello')

    def display():
        print(A.__a)
        A.__fn()

A.display()
```

#### Example of a bank

Private variable PIN Example :

```python
class Bank:
    def __init__(self,bal,pin):
        self.bal = bal
        self.__pin = pin

    def checkpin(self,pin):
        if self.__pin == pin:
            return True
        else:
            print('Invalid Pin')

    def withdraw(self,amt,pin):
        if self.checkpin(pin):
            self.bal = self.bal - amt
            print('Withdraw Done')
            print('Balance:', self.bal)

c = Bank(100,2020)
c.withdraw(50,2021)
```

### Private method example

Private method showBalance example:

```python
class Bank:
    def __init__(self,bal,pin):
        self.bal = bal
        self.__pin = pin

    def checkpin(self,pin):
        if self.__pin == pin:
            return True
        else:
            print('Invalid Pin')

    def __showbalance(self):
        print(self.bal)

    def checkbalance(self,pin):
        if self.checkpin(pin):
            self.__showbalance()

c = Bank(100,2020)
c.checkbalance(2020)
```


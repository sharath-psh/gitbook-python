# Object Method

```python
class A:
    def disp(self):
        print(self.a)

obj1 = A()
obj1.a = 10
obj1.disp()
```

```python
class Bank:
    def __init__(self,name,bal):
        self.name = name
        self.bal = bal

    def deposit(self,amt):
        self.bal = self.bal + amt

ram = Bank('ram',100)

ram.deposit(10)
print(ram.bal)
```

* Object methods are functions created inside the class, for the purpose of objects
* self in the object method will be pointing to the called object.
* classes cannot call object methods

Errors Classes cannot access object methods Ex: A.disp\(\) TypeError: disp\(\) missing 1 required positional argument: 'self'


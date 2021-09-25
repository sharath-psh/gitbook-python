# Constructor

* Constructors or initialisers help us in creating objects.

Simple constructor Example:

```python
class Demo:                     # creating a class Demo
    def __init__(self,a):       # constructor accepting argument 'a'
        self.a = a              # assining arg 'a' to the object

obj = Demo(1)           # creating the object 'obj' for the class'Demo'
                        # object data '1' being sent to the arg 'a'
print(obj.a)            # printing the obj data 

# o/p -->
# 1
```

## Object data creation

Before using the help of constuctors:

```python
class Company:
    c_name = 'Tata'
    branch = 'BLR'

ram = emp()
sam = emp()

ram.id = 322
ram.sal = 10000
ram.name = 'Ram'

sam.id = 323
sam.sal = 20000
sam.name = 'Sam'

print(ram.id, ram.c_name)
print(sam.id, sam.c_name)

# o/p -->
# 322 Tata
# 323 Tata
```

After using constructors

```python
class Company:
    c_name = 'Tata'
    branch = 'BLR'

    def __init__(self,id,sal,name):
        self.id = id
        self.sal = sal
        self.name = name

ram = Company(322,10000,'Ram')
sam = Company(323,20000,'Sam')

print(ram.id, ram.c_name)
print(sam.id, sam.c_name)

# o/p -->
# 322 Tata
# 323 Tata
```

* Constructor or initilizer is a special inbuilt function in python which helps us to create object data.

Syntax :

```python
class class_name:
    def __init__(self,args):
        self.var = arg

object_name = class_name(arg)
```

* constructor is created inside the class
* \__init\__ the double underscore in python is called as 'dunder'
* these methods are also called as magic methods, these are special methods in python which start and end with double underscore.
* the first argument of a constructor _must_ be self.
* constructor is invoked everytime we create an object.
* self refers to the _object_ which is calling.
* we can give _any_ name instead of self, but in python it is common to use 'self'.
* we do not need to pass the object name in the argument. Python automatically considers the object name as self.
* the variables created inside the object can only be accessed by the reffered object in self.
* constructor is optional.

Errors:

* Not mentioning self will raise an error related to the arguments in the function. where an additional actual arguments are passed but the formal arguments are less. TypeError: class\(\) takes 0 positional arguments but 1 was given
* During object creation when an constructor is not created, but if arguments are passed we get the error: TypeError: class\(\) takes no arguments


# Single Inheritance

### Single Inheritance with 2 classes and class data

```python
class parent:
    a = 1

class child(parent):
    b = 2

print(parent.a)
print(child.a)
# print(parent.b)
print(child.b)

# o/p --->
# 1
# 1
# 2
```

## Single inheritance

Syntax:

```python
class parent_CN:          # CN >> classname
    ----
    ----
class child_CN(parent_CN):
    -----
    -----
```

* All the class data from the parent is passed on to the child class.
* child class can access all the data of the parent class as well as its own class.
* parent class can only access data of itself, it cannnot access the data of child class.

Errors:

* parent class accessing child class data, will give error:

  AttributeError: type object 'c1' has no attribute 'b'

### Single Inheritance with object data

```python
class parent:
    a = 1

class child(parent):
    b = 2

par_obj = parent()
chi_obj = child()

print(par_obj.a)
print(chi_obj.a,chi_obj.b)

# o/p --->
# 1
# 1 2
```

* just like how the child class was able to access parent class data, but not the other way around.
* similarly, child class can access parent class object data.
* but the parent class cannot access child class object data.

### Single Inheritance with object data

#### with same obj data var name as parent class

```python
class parent:
    a = 1

class child(parent):
    a = 55
    b = 2

par_obj = parent()
chi_obj = child()

print(parent.a)
print(child.a, child.b)

print(par_obj.a)
print(chi_obj.a,chi_obj.b)

# o/p --->
# 1
# 55 2
# 1
# 55 2
```

### Single inheritance method overriding

```python
class A:
    def fn():
        print('FN in A')

class B(A):
    pass

A.fn()
B.fn()

# o/p
# FN in A
# FN in A
```

```python
class A:
    def fn():
        print('FN in A')

class B(A):
    def fn():
        print('FN in B')

A.fn()
B.fn()

# o/p
# FN in A
# FN in B
```

### Single inheritance with constructor

```python
class parent:
    def __init__(self,a):
        self.a = a

class child(parent):
    pass

par_obj = parent(1)
chi_obj = child(2)

print(par_obj.a)
print(chi_obj.a)

# o/p --->
# 1
# 2
```

* when we inherit the properties of the parent class to child class, we note some important things.
* all the properties gets inherited. including the constructor
* since the constructor is also passed on, we need to pass an arg.
* when we create a child class object\(chi\_obj\), we should pass an argument which will be stored in the child class object itself.

Errors: if in the child class object \(chi\_obj\) we do not pass the argument we get the error: Ex: chi\_obj = child\(\)

TypeError: **init**\(\) missing 1 required positional argument: 'a'

### Single inheritance method overriding

```python
class parent:
    def __init__(self,a):
        self.a = a

class child(parent):
    def __init__(self,a):
        self.a = a

par_obj = parent(1)
chi_obj = child(2)

print(par_obj.a)
print(chi_obj.a)

# o/p --->
# 1
# 2
```

```python
class parent:
    def __init__(self,a,b):
        self.a = a
        self.b = b

    @staticmethod
    def printer(sum):
        print(sum)

    def add(self):
        sum = self.a + self.b
        self.printer(sum)

class child(parent):
    pass

o = parent(1,2)
o.add()

o2 = child(2,4)
o2.add()

# o/p --->
# 3
# 6
```

```python
class parent:
    def __init__(self,a,b):
        self.a = a
        self.b = b

    @staticmethod
    def printer(sum):
        print(sum)

    def add(self):
        sum = self.a + self.b
        self.printer(sum)

class child(parent):
    def __init__(self,a,b):
        self.a = a
        self.b = b

    @staticmethod
    def printer(sum):
        print(sum)

    def sub(self):
        sum = self.a - self.b
        self.printer(sum)

o = parent(1,2)
o.add()

o2 = child(2,4)
o2.add()
o2.sub()

# o/p --->
# 3
# 6
# -2
```

### super keyword

```python
class A:
    def fn(self):
        print('FN in A')

class B(A):
    def fn(self):
        super().fn()
        print('FN in B')

par_obj = A()

# par_obj.fn()

chi_obj = B()
chi_obj.fn()
```


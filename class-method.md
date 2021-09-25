# Class Method

```python
class Demo:
    a = 1
    @classmethod
    def disp_cls(cls):
        print(cls.a)


Demo.disp_cls()
obj1 = Demo()
obj1.disp_cls()

# o/p -->
# 1
```

Classmethod is used to access and modify class data

Syntax:

```python
class class_name:
    var = value
    @classmethod
    def function_name(cls,args):
        print(cls.var)
class_name.function_name(args)
```

* a class method is used to access and modify the class data
* to create a class method inside a class, we use

  @classmethod

  which is called as a annotation/decorator.

* a class method has a mandatory argument of 'cls', which helps

  us access the class.

* while accessing the class data also, we should use 'cls'.
* in a classmethod instead of 'self' we use 'cls'.
* similar to self, we can use anything as the first argument
* an object or a class can call a classmethod.
* we use this in order to avoid creating an object just to modify

  the class data, saving memory and an instance\(i.e. creating a new

  object just for the sake of modifying class data\)

* we can use this classmethod n number of times since this is a

  function specifically designed for modifying and access cls data.

Errors: classmethod cannnot access object data


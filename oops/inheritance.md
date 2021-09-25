# Inheritance

```python
class parent:
    a = 1

class child(parent):
    pass

print(parent.a)
print(child.a)

# o/p --->
# 1
# 1
```

* deriving data from one class to another class is called as inheritance

Syntax:

```python
class parent_CN:          # CN >> classname
    ----
    ----
class child_CN(parent_CN):
    -----
    -----
```

* used to reduce code and save memory
* inheritance enables extending the capability of an existing class to build a new class, instead of building from scratch
* used to derive parent class data to child class.
* In order establish the relation between the classes, we use the syntax: child\_class\(parent\_class\)
* the class from which we iherit/derive the data is called

  as parent/super/base class

* the class which gets the data is called as

  child/sub/derived class

* when we inherit from the parent, we inherit all the class data and its methods

Types of Inheritance:

1. Single Level Inheritance
2. Multilevel Inheritance
3. Hierchial Inheritance
4. Multiple Inheritance
5. Hybrid Inheritance


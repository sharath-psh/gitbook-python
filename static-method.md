# Static Method

```python
class Demo:
    @staticmethod
    def fn():
        print('hello')
Demo.fn()
obj = Demo()
obj.fn()
```

Syntax:

```python
class class_name:
    @staticmethod
    def function_name():
        print('hello')
class_name.function_name()
```

* a function which can be accessed by both class and object
* used to create functions which does not require any 'self' or 'cls' args.
* can be used to do a independant function which does not require the class data or object data
* best used like a function, where we can pass args and it gives us a return val.
* we use the annotation '@staticmethod' to create a static function.
* class can access staticmethod,even if annotation is not given.
* objects cannot access staticmethods, unless annotation is given.

Errors if a object access a function which does not have staticmethod annotation, it gives args error Ex: class Demo: def fn\(\): print\('hello'\)

obj1 = Demo\(\) obj1.fn\(\) o/p ---&gt; TypeError: fn\(\) takes 0 positional arguments but 1 was given '''


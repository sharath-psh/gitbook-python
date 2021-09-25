# Class and Object Data

Class creation :

* class class\_name:
* when python sees the keyword called class, it will create a dictionary block in the memory. in the form of key,value pairs of variables and its values.
* we store all our functions and variables inside our class.
* class name follows the same rules as identifier rules.It is not nessasary for class name to be in capitals.
* can have docstrings.

Syntax :

```python
class class_name:
    -------------
    Variables/Functions
    -------------
object_name = class_name()
```

* Simple class example

```python
class Demo:
    a = 1
obj1 = Demo()
print(obj1.a)

# o/p -> 1
```

Here variable 'a' is class data which is derived to the object 'obj1'. 'obj1' is in an instance\(object\) of class 'Demo'.

## Class with class data

Example of a class with class data and objects.

```python
class car:
    wheels = 4
    steering = 'automatic'
    gears = 5

mahi = car()
tata = car()


print('car :: wheels', car.wheels,',steering : ', car.wheels,',gears : ', car.wheels)
print('mahi car :: wheels', mahi.wheels,',steering : ', mahi.wheels,',gears : ', mahi.wheels)
print('tata car :: wheels', tata.wheels,',steering : ', tata.wheels,',gears : ', tata.wheels)

# o/p -->
# car :: wheels 4 ,steering :  4 ,gears :  4     
# mahi car :: wheels 4 ,steering :  4 ,gears :  4
# tata car :: wheels 4 ,steering :  4 ,gears :  4
```

Car class with class data where the properties of car apply to all types of cars\(in this case our objects\)

The class data is inherited to the object

Errors: If we do not mention the class name or object name when accessing the data we get the error: 'var' is not defined.

## Class with object data

Example of class with object data. Modification of object data and class data.

```python
class car:
    wheels = 4
    steering = 'automatic'
    gears = 5

mahi = car()
tata = car()

car.gears = 6


print('car :: wheels', car.wheels,',steering : ', car.steering,',gears : ', car.gears)
print('mahi car :: wheels', mahi.wheels,',steering : ', mahi.steering,',gears : ', mahi.gears)
print('tata car :: wheels', tata.wheels,',steering : ', tata.steering,',gears : ', tata.gears)


mahi.fuel = 'petrol'
mahi.range = 40

tata.fuel = 'diesel'
tata.range = 50

print('mahi gear' , mahi.gears)
print(mahi.fuel)
print(mahi.range)
print(tata.fuel)
print(tata.range)

# o/p --->
# car :: wheels 4 ,steering :  automatic ,gears :  6     
# mahi car :: wheels 4 ,steering :  automatic ,gears :  6
# tata car :: wheels 4 ,steering :  automatic ,gears :  6
# mahi gear 6
# petrol
# 40
# diesel
# 50
```

* Modifying class data changes the data of the object too.
* Modifying object data does not affect the class data, or other objects.

> Syntax : to create/modify object data object\_name.variable = value to access object data object\_name.variable


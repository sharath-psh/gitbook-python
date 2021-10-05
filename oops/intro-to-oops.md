# Introduction to OOPs

## What is OOP?

- Python supports scripting, functions and also object oriented programming.
- Object Oriented Programming is where we write our code in the form of classes and objects.
- Where objects represent any real world entity with data and functions.
- Classes act as a blueprint for the objects.

## Classes and Data are classified as follows

### Data

- Class Data : Data which is generic and applicable to all the objects.

  Generic data.

- Object Data : Data which is specific and applicable only to the objects.

  Instance/Object variables/data.

  Attributes.

### Functions/Methods

- Object Method : Functions which are specific only for the objects.

  Instance method/function.

  Behaviour of the object.

- Class Method : Function designed for modifying class data.
- Static Method : A simple function irrespective of classes or objects calling.

### Examples of Class

1.Bank Class :

class : Bank class data : branch, bank name, rate of interest, Object : Bank customers can be as objects. Ex: Ram, Sam, Shyam. Object data : Customer data like balance, name, id. Ex: customer balance, customer name, customer id.

Class method : Changing the banks rate of interest, branch location. Object method : Customer related functions like withdraw, balance check, deposit.

2.Company Class:

class : Company class data : branch, Company name, revenue, profits, stock ticker. Object : Employees. Ex: Ram, Sam, Shyam. Object data : Employee data like salary, name, pin, id. Ex: employee balance, employee name, employee id.

Class method : class functions can be stock price, revenue changes. Object method : employee status, salary updation, current project, reporting manager, team.

## Comparison of program with and without using class

Object Oriented approch :

```python
class Student(object):
    def __init__(self, name, age, gender, level, grades=None):
        self.name = name
        self.age = age
        self.gender = gender
        self.level = level
        self.grades = grades or {}

    def setGrade(self, course, grade):
        self.grades[course] = grade

    def getGrade(self, course):
        return self.grades[course]

    def getGPA(self):
        return sum(self.grades.values())/len(self.grades)

# Define some students
john = Student("John", 12, "male", 6, {"math":3.3})
jane = Student("Jane", 12, "female", 6, {"math":3.5})

# Now we can get to the grades easily
print(john.getGPA())
print(jane.getGPA())
```

Standard Programming :

```python
def calculateGPA(gradeDict):
    return sum(gradeDict.values())/len(gradeDict)

students = {}
# We can set the keys to variables so we might minimize typos
name, age, gender, level, grades = "name", "age", "gender", "level", "grades"
john, jane = "john", "jane"
math = "math"
students[john] = {}
students[john][age] = 12
students[john][gender] = "male"
students[john][level] = 6
students[john][grades] = {math:3.3}

students[jane] = {}
students[jane][age] = 12
students[jane][gender] = "female"
students[jane][level] = 6
students[jane][grades] = {math:3.5}

# At this point, we need to remember who the students are and where the grades are stored. Not a huge deal, but avoided by OOP.
print(calculateGPA(students[john][grades]))
print(calculateGPA(students[jane][grades]))
```

## Why is OOPs used?

- Organize code and classify data and functions providing a clear structure.
- Easy maintainence and modification.
- Reduce code, by enabling code reusability.
- Inheritance, which helps us to inherit data from one class to another class.
- Encapsulation, where we secure data by implementing private variables.

## Where do we use OOPs?

- When we have a large project and the codebase needs to be organised.
- Enabling us with easy maintainance and modification
- Decreasing redundant data by using OOPs concepts like inheritance, class data, objects.
- Protecting data which should not be accessed outside the class. Ex: keys, pins, passwords, private variables.

## How to create a class?

Simple example of a class with a object.

```python
class Demo:
    a = 1
obj = Demo()
print(obj.a)
```

## Glossary

- Class : Blueprint to create the classes.
- Object : Real world entity created using the class.
- Instance : Refers to the object created from the class.
- Method : Functions created inside a class.
- Attribute : Refers to the object or class data.
- Initialiser/Constructor/Init method : constructer/\_\_init\_\_ is a reserved method which is created in the class beginning to help us create objects.
  It helps us in creating object data.
- self : refers to the address of the object. must be used when we store object related data. -
- private : protecting data by not allowing to access it outside the class.
- encapsulation : refers to the hiding of data
- inheritance : where we are able to provide the code from one class to another.

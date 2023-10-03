## Use the super() Function
Python also has a `super()` function that will make the child class inherit all the methods and properties from its parent:

```python
class Person:
  def __init__(self, fname, lname): #constructor
    self.firstname = fname
    self.lastname = lname

  def printname(self):  # method
    print(self.firstname, self.lastname)

class Student(Person):  # child class
  def __init__(self, fname, lname):
    super().__init__(fname, lname)

x = Student("Mike", "Olsen")
x.printname()
```

Output:
```
Mike Olsen
```

By using the `super()` function, you do not have to use the name of the parent element, it will automatically inherit the methods and properties from its parent.

## Add Properties:
#### - Add a property called `graduationyear` to the `Student` class:

```python
class Person:
  def __init__(self, fname, lname): #constructor
    self.firstname = fname
    self.lastname = lname

  def printname(self): # method
    print(self.firstname, self.lastname)

class Student(Person): # child class
  def __init__(self, fname, lname):
    super().__init__(fname, lname)
    self.graduationyear = 2019 #property

x = Student("Mike", "Olsen")
print(x.graduationyear)
```

Output:
```
2019
```
In the example below, the year `2019` should be a variable, and passed into the `Student` class when creating student objects. To do so, add another parameter in the __init__() function.

---
#### - Add a `year` parameter, and pass the correct year when creating objects:

```python
class Person:
  def __init__(self, fname, lname): #constructor
    self.firstname = fname
    self.lastname = lname

  def printname(self): # method
    print(self.firstname, self.lastname)

class Student(Person): # child class
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year #property

x = Student("Mike", "Olsen", 2019)
print(x.graduationyear)
```

Output:
```
2019
```

## Add Methods:
Add a method called `welcome` to the `Student` class:

```python
class Person:
  def __init__(self, fname, lname): #constructor
    self.firstname = fname
    self.lastname = lname

  def printname(self): # method
    print(self.firstname, self.lastname)

class Student(Person): # child class
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year
 
  def welcome(self):  # method
    print("Welcome", self.firstname, self.lastname, "to the class of", self.graduationyear)

x = Student("Mike", "Olsen", 2019)
x.welcome()
```

Output:
```
Welcome Mike Olsen to the class of 2019
```
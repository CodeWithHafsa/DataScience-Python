# Python Inheritance
Inheritance allows us to define a class that inherits all the methods and properties from another class.
* Parent class => is the class being inherited from, also called base class.
* Child class => is the class that inherits from another class, also called derived class.

## Types of Inheritance
1. **Single Inheritance**: Single-level inheritance enables a derived class to inherit characteristics from a single-parent class.
2. **Multilevel Inheritance**: Multi-level inheritance enables a derived class to inherit properties from an immediate parent class which in turn inherits properties from his parent class. 
3. **Hierarchical Inheritance**: Hierarchical-level inheritance enables more than one derived class to inherit properties from a parent class.
4. **Multiple Inheritance**: Multiple-level inheritance enables one derived class to inherit properties from more than one base class.

## Create a Parent Class
Any class can be a parent class, so the syntax is the same as creating any other class:

*Example*:

Create a class named `Person`, with `firstname` and `lastname` properties, and a `printname` method:
```python
class Person:
  def __init__(self, fname, lname): # constructor
    self.firstname = fname
    self.lastname = lname

  def printname(self):  # method
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:
x = Person("John", "Doe") #object

# calling the method
x.printname()
```

Output:
```
John Doe
```

## Create a Child Class
To create a class that inherits the functionality from another class, send the parent class as a parameter when creating the child class:

*Example 01*:
Create a class named `Student`, which will inherit the properties and methods from the `Person` class:
```python
class Student(Person):
  pass 

# Use the pass keyword when you do not want to add any other properties or methods to the class
# The Student class has the same properties and methods as the Person class.
```

=======================================================
*Example 02*:

```python
class Person:
  def __init__(self, fname, lname):  # constructor
    self.firstname = fname
    self.lastname = lname

  def printname(self):  # method
    print(self.firstname, self.lastname)

class Student(Person):
  pass

# calling the method
x = Student("Mike", "Olsen")
x.printname()
```

Output:
```
Mike Olsen
```
=======================================================
*Example 03*: We want to add the `__init__()` function to the child class (instead of the pass keyword).

```python
class Student(Person):
  def __init__(self, fname, lname):
    #add properties etc.
```

#### Note: 
The child's __init__() function overrides the inheritance of the parent's __init__() function. To keep the inheritance of the parent's __init__() function, add a call to the parent's __init__() function:

```python
class Person:
  def __init__(self, fname, lname): # constructor
    self.firstname = fname
    self.lastname = lname

  def printname(self):  # method
    print(self.firstname, self.lastname)

class Student(Person):  #child class
  def __init__(self, fname, lname):
    Person.__init__(self, fname, lname)

x = Student("Mike", "Olsen")
x.printname()
```

Output:
```
Mike Olsen
```

## Create a Parent / Child Inheritance Class Example:

```python
class Father(): 
    def __init__(self): # constructor
        self.eye_color = None
    
    def speaking(self,words): # method
        print(f"Father function....{words}")
    
class Mother():
    def __init__(self): # constructor
        self.hair_color = None
    
    def looking(self): # method
        print("Monther function... Mother looking function")
        
        
class Children(Father, Mother): #calling 
    pass

c1 = Children()
c1.speaking("Hello world")
c1.looking()
```

Output:
```
Father function....Hello world
Monther function... Mother looking function
```

## Example:
```python
# base class
class Animal:
    
    def eat(self):
        print( "I can eat!")
    
    def sleep(self):
        print("I can sleep!")

# derived class
class Dog(Animal):
    
    def bark(self):
        print("I can bark! Woof woof!!")

# Create object of the Dog class
dog1 = Dog()

# Calling members of the base class
dog1.eat()
dog1.sleep()

# Calling member of the derived class
dog1.bark()

# Calling members of the Animal class
# dog1.eat()
# dog1.sleep()
```

Output:
```
I can eat!
I can sleep!
I can bark! Woof woof!!
```

#### NOTE:
* Use dir(c1) => to know all the methods and attibutes
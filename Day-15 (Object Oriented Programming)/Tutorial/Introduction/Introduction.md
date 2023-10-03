# Object Oriented Programming:
In Python, object-oriented Programming (OOPs) is a programming paradigm that uses objects and classes in programming. It aims to implement real-world entities like inheritance, polymorphisms, encapsulation, etc. in the programming. 

The main concept of OOPs is to bind the data and the functions that work on that together as a single unit so that no other part of the code can access this data.

Python is an object oriented programming language. Almost everything in Python is an object, with its properties and methods.

## OOPs Concepts in Python:
* Class
* Objects
* Polymorphism
* Encapsulation
* Inheritance
* Data Abstraction

## Python Classes:
A Class is like an object constructor, or a "blueprint" for creating objects.\
It is a logical entity that contains some attributes and methods.

* Classes are created by keyword class.
* Attributes are the variables that belong to a class.
* Attributes are always public and can be accessed using the dot (.) operator. Eg.: Myclass.Myattribute

### Create a Class: 
To create a class, use the keyword class:
```python
class MyClass:
  x = 5

print(MyClass)
```

Output:
```
<class '__main__.MyClass'>
```

## Python Objects:
The object is an entity that has a state and behavior associated with it. It may be any real-world object like a mouse, keyboard, chair, table, pen, etc. Integers, strings, floating-point numbers, even arrays, and dictionaries, are all objects.

An object consists of:

* **State**: It is represented by the attributes of an object. It also reflects the properties of an object.
* **Behavior**: It is represented by the methods of an object. It also reflects the response of an object to other objects.
* **Identity**: It gives a unique name to an object and enables one object to interact with other objects.

### Create Object:
Now we can use the class named MyClass to create objects:
```python
class MyClass:
  x = 5

p1 = MyClass()
print(p1.x)
```

Output:
```
5
```

## The __init__() Function:
All classes have a function called __init__(), which is always executed when the class is being initiated. 

The __init__() function is called automatically every time the class is being used to create a new object.\
In Python the __init__() method is called the constructor and is always called when an object is created.

Use the __init__() function to assign values to object properties, or other operations that are necessary to do when the object is being created.

**Syntax**:
```python
def __init__(self):
    # body of the constructor
```

## Types of constructors : 

* **default constructor**: The default constructor is a simple constructor which doesn’t accept any arguments. Its definition has only one argument which is a reference to the instance being constructed.
* **parameterized constructor**: constructor with parameters is known as parameterized constructor. The parameterized constructor takes its first argument as a reference to the instance being constructed known as self and the rest of the arguments are provided by the programmer.

### Example:
```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
```

Output:
```
John
36
```

## The __str__() Function:
The __str__() function controls what should be returned when the class object is represented as a string.

If the __str__() function is not set, the string representation of the object is returned:

* Without __str__() Function:

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1)

# Output: <__main__.Person object at 0x15039e602100>
```


* With __str__() Function:
```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def __str__(self):
    return f"{self.name}({self.age})"

p1 = Person("John", 36)

print(p1)
```

Output:
```
John(36)
```

## Object Methods:
Objects can also contain methods. Methods in objects are functions that belong to the object.

*Example*:

Insert a function that prints a greeting, and execute it on the p1 object:
```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()
```

Output:
```
Hello my name is John
```

## The self Parameter:
The **self** parameter is a reference to the current instance of the class, and is used to access variables that belongs to the class.

It does not have to be named **self** , you can call it whatever you like, but it has to be the first parameter of any function in the class:

*Example*:

Use the words 'mysillyobject' and 'abc' instead of self:
```python
class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()
```

Output:
```
Hello my name is John
```

## Modify Object Properties:
You can modify properties on objects like this:

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)

p1.age = 40

print(p1.age)
```

Output:
```
40
```

## Delete Object Properties:
You can delete properties on objects by using the **del** keyword:

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)

del p1.age

print(p1.age)

#Output: AttributeError: 'Person' object has no attribute 'age'
```

## Delete Objects:
You can delete objects by using the **del** keyword:

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)

del p1

print(p1)

#Output: NameError: 'p1' is not defined
```

## The pass Statement:
**class** definitions cannot be empty, but if you for some reason have a **class** definition with no content, put in the **pass** statement to avoid getting an error.

```python
class Person:
  pass

# having an empty class definition like this, would raise an error without the pass statement
```

## Example: Python Class and Object
```python
class Parrot:

    # class attribute
    name = ""
    age = 0

# create parrot1 object
parrot1 = Parrot()
parrot1.name = "Blu"
parrot1.age = 10

# create another object parrot2
parrot2 = Parrot()
parrot2.name = "Woo"
parrot2.age = 15

# access attributes
print(f"{parrot1.name} is {parrot1.age} years old")
print(f"{parrot2.name} is {parrot2.age} years old")
```

Output:
```
Blu is 10 years old
Woo is 15 years old
```
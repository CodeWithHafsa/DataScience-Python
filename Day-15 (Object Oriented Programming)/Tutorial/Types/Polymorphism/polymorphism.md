# What is Polymorphism: 
The word polymorphism means having many forms. In programming, polymorphism means the same function name (but different signatures) being used for different types. The key difference is the data types and number of arguments used in function.

## Example of inbuilt polymorphic functions:
```python
# Python program to demonstrate in-built polymorphic functions
 
# len() being used for a string
print(len("geeks"))
 
# len() being used for a list
print(len([10, 20, 30]))
```

Output:
```
5
3
```
Note:  In this case, `len("geeks")` returns `5` because the string “geeks” has 5 characters, while `len([10, 20, 30])` returns `3` because the list contains 3 elements.


## Examples of user-defined polymorphic functions: 
```python

# A simple Python function to demonstrate Polymorphism
 
def add(x, y, z = 0):
    return x + y + z
 
# Driver code
print(add(2, 3))
print(add(2, 3, 4)) #add all numbers
```

Output:
```
5
9
```

## Polymorphism with class methods: 

*Example 01* :
```python
#  Creating class1
class Pakistan(): 
    def capital(self): #method1
        print("Islamabad is the capital of Pakistan.")
  
    def language(self): #method2
        print("Urdu is the most widely spoken language of Pakistan.")
 
    def type(self): #method2
        print("Pakistan is a developing country.")
 
#  Creating class2
class USA():  
    def capital(self): #method1
        print("Washington, D.C. is the capital of USA.")
 
    def language(self): #method2
        print("English is the primary language of USA.")
  
    def type(self): #method3
        print("USA is a developed country.")
 
obj_ind = Pakistan()  #object 1
obj_usa = USA()    #object 2

# Calling the method
# Calling all three methods for both methods with the help of loop.
for country in (obj_ind, obj_usa): 
    country.capital()
    country.language()
    country.type()

# Calling all three methods for both methods individually.
# obj_ind.capital()  # Output: Islamabad is the capital of Pakistan.
# obj_ind.language()  # Output: Urdu is the most widely spoken language of Pakistan.
# obj_ind.type()  # Output: Pakistan is a developing country.

# obj_usa.capital()  # Output: Washington, D.C. is the capital of USA.
# obj_usa.language()  # Output: English is the primary language of USA.
# obj_usa.type()  # Output: USA is a developed country.

```

Output:
```
Islamabad is the capital of Pakistan.
Urdu is the most widely spoken language of Pakistan.
Pakistan is a developing country.
Washington, D.C. is the capital of USA.
English is the primary language of USA.
USA is a developed country.
```
========================================================
*Example 02* :
```python
class Polygon:
    # method to render a shape
    def render(self):
        print("Rendering Polygon...")

class Square(Polygon):
    # renders Square
    def render(self):
        print("Rendering Square...")

class Circle(Polygon):
    # renders circle
    def render(self):
        print("Rendering Circle...")
    
# create an object of Square
s1 = Square()
s1.render()

# create an object of Circle
c1 = Circle()
c1.render()
```

Output:
```
Rendering Square...
Rendering Circle...
```
Note: In the above example, we have created a superclass: Polygon and two subclasses: Square and Circle. Notice the use of the render() method.\
The main purpose of the render() method is to render the shape. However, the process of rendering a square is different from the process of rendering a circle.\
Hence, the render() method behaves differently in different classes. Or, we can say render() is polymorphic.

========================================================
*Example 03* :
```python
class Cat:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def info(self):
        print(f"I am a cat. My name is {self.name}. I am {self.age} years old.")

    def make_sound(self):
        print("Meow")

class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def info(self):
        print(f"I am a dog. My name is {self.name}. I am {self.age} years old.")

    def make_sound(self):
        print("Bark")

cat1 = Cat("Kitty", 2.5)
dog1 = Dog("Fluffy", 4)

for animal in (cat1, dog1):
    animal.make_sound()
    animal.info()
    animal.make_sound()
```

Output:
```
Meow
I am a cat. My name is Kitty. I am 2.5 years old.
Meow
Bark
I am a dog. My name is Fluffy. I am 4 years old.
Bark
```

## Types of Polymorphism
There are two parts/types of Polymorphism:
1. Overriding
2. Overloading

Overloading and Overriding in Python are the two main object-oriented concepts that allow programmers to write methods that can process a variety of different types of functionalities with the same name.

## Method Overloading in Python:
Method Overloading in Python is a type of Compile-time Polymorphism using which we can define two or more methods in the same class with the same name but with a different parameter list.

We cannot perform method overloading in the Python programming language as everything is considered an object in Python. It uses the latest definition for the method. 

*Example 01* :
```python
# Function to take multiple arguments
def sum_number(*args):
    # variable to store the sum of numbers    
    result = 0
    
    # accessing the arguments
    for num in args:
        result += num
    
    # Output
    print("Sum : ", result)

    
# Driver Code
if(__name__ == "__main__"):
    print("Similar to Method Overloading\n")
    print("Single Argument    ->", end = " ")
    sum_number(10)

    print("Two Arguments      ->", end = " ")
    sum_number(30, 2)

    print("Multiple Arguments ->", end = " ")
    sum_number(1, 2, 3, 4, 5)
```

Output:
```
Similar to the Method of Overloading

Single Argument    -> Sum :  10
Two Arguments      -> Sum :  32
Multiple Arguments -> Sum :  15
```

========================================================
*Example 02* :
```python
# Function to take multiple arguments
def add(datatype, *args):
   
    # if datatype is int
    # initialize answer as 0
    if datatype =='int':
        answer = 0
           
    # if datatype is str
    # initialize answer as ''
    if datatype =='str':
        answer =''
   
    # Traverse through the arguments
    for x in args:
   
        # This will do addition
        #  if the arguments are int. Or concatenation 
        # if the arguments are str
        answer = answer + x
   
    print(answer)
   
# Integer
add('int', 5, 6)
   
# String
add('str', 'Hi ', 'Geeks')
```

Output:
```
11
Hi Geeks
```

## Method Overriding in Python:
Method Overriding is a type of Run-time Polymorphism. A child class method overrides (or provides its implementation) the parent class method of the same name, parameters, and return type. It is used to over-write (redefine) a parent class method in the derived class. 

It is used to change the behavior of existing methods and there is a need for at least two classes for method overriding.

*Example 01*:
```python
# Parent Class
class A:
    def first(self):
        print("First function of class A")

    def second(self):
        print('Second function of class A')

# Derived Class
class B(A):
    # Overriden Function
    def first(self):
        print("Redefined function of class A in class B")

    def display(self):
        print('Display Function of Child class')

# Driver Code
if(__name__ == "__main__"):
    # Creating child class object
    child_obj = B()
    
    # Calling the overridden method
    print("Method Overriding\n")
    child_obj.first()
    
    # Calling the original Parent class method
    # Using parent class object.
    A().first()
```

Output:
```
Method Overriding

Redefined function of class A in class B
First function of class A
```

========================================================
*Example 02* :
```python
class A:
 
    def fun1(self):
        print('feature_1 of class A')
         
    def fun2(self):
        print('feature_2 of class A')
     
 
class B(A):
     
    # Modified function that is
    # already exist in class A
    def fun1(self):
        print('Modified feature_1 of class A by class B')   
         
    def fun3(self):
        print('feature_3 of class B')
         
 
# Create instance
obj = B()
     
# Call the override function
obj.fun1()
```

Output:
```
Modified feature_1 of class A by class B
```
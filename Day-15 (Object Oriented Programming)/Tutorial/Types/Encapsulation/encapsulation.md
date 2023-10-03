# Encapsulation in Python
Encapsulation is one of the fundamental concepts in object-oriented programming (OOP). It describes the idea of wrapping data and the methods that work on data within one unit. This puts restrictions on accessing variables and methods directly and can prevent the accidental modification of data. To prevent accidental change, an object’s variable can only be changed by an object’s method. Those types of variables are known as private variables.

In Python, we denote private attributes using underscore as the prefix i.e single underscore _ or double underscore __.

## Examples:

####  *Example 01 - Protected members*
Protected members (in C++ and JAVA) are those members of the class that cannot be accessed outside the class but can be accessed from within the class and its subclasses. 

```python
# Python program to demonstrate protected members
  
class Base:  # Creating a base class
    def __init__(self):
  
        # Protected member
        self._a = 2
  
class Derived(Base):  # Creating a derived class
    def __init__(self):
  
        # Calling constructor of Base class
        Base.__init__(self)
        print("Calling protected member of base class: ", 
              self._a)
  
        # Modify the protected variable:
        self._a = 3
        print("Calling modified protected member outside class: ",
              self._a)
  
  
obj1 = Derived()
  
obj2 = Base()
  
# Calling protected member
# Can be accessed but should not be done due to convention
print("Accessing protected member of obj1: ", obj1._a)
  
# Accessing the protected variable outside
print("Accessing protected member of obj2: ", obj2._a)
```

Output:
```
Calling protected member of base class:  2
Calling modified protected member outside class:  3
Accessing protected member of obj1:  3
Accessing protected member of obj2:  2
```

=========================================================
#### *Example 02 - Private members*
Private members are similar to protected members, the difference is that the class members declared private should neither be accessed outside the class nor by any base class. In Python, there is no existence of Private instance variables that cannot be accessed except inside a class.

However, to define a private member prefix the member name with double underscore “__”.

```python

# Python program to demonstrate private members
  
class Base: # Creating a Base class
    def __init__(self):
        self.a = "GeeksforGeeks"
        self.__c = "GeeksforGeeks"
  
class Derived(Base):  # Creating a derived class
    def __init__(self):
  
        # Calling constructor of Base class
        Base.__init__(self)
        print("Calling private member of base class: ")
        print(self.__c)
  
  
# Driver code
obj1 = Base()
print(obj1.a)
  
# Uncommenting print(obj1.c) will raise an AttributeError
  
# Uncommenting obj2 = Derived() will also raise an AttributeError as private member of base class is called inside derived class
```

Output:
```
GeeksforGeeks
```

*Example 03*: 
```python
class Computer:

    def __init__(self):
        self.__maxprice = 900

    def sell(self):
        print("Selling Price: {}".format(self.__maxprice))

    def setMaxPrice(self, price):
        self.__maxprice = price

c = Computer()
c.sell()

# change the price
c.__maxprice = 1000
c.sell()

# using setter function
c.setMaxPrice(1000)
c.sell()
```

Output:
```
Selling Price: 900
Selling Price: 900
Selling Price: 1000
```

Note: Here, we have tried to modify the value of __maxprice outside of the class. However, since __maxprice is a private variable, this modification is not seen on the output.

As shown, to change the value, we have to use a setter function i.e setMaxPrice() which takes price as a parameter.
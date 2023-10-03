# Abstract Classes in Python:
An abstract class can be considered a blueprint for other classes. It allows you to create a set of methods that must be created within any child classes built from the abstract class. 

*Example 01* :
```python
# Python program showing abstract base class work
from abc import ABC, abstractmethod
 
class Polygon(ABC):
    @abstractmethod
    def noofsides(self):
        pass
 
class Triangle(Polygon):
    # overriding abstract method
    def noofsides(self):
        print("I have 3 sides")
 
 
class Pentagon(Polygon):
    # overriding abstract method
    def noofsides(self):
        print("I have 5 sides")
 
 
class Hexagon(Polygon):
    # overriding abstract method
    def noofsides(self):
        print("I have 6 sides")
 
 
class Quadrilateral(Polygon):
    # overriding abstract method
    def noofsides(self):
        print("I have 4 sides")
 
 
# Driver code
R = Triangle()
R.noofsides()
 
K = Quadrilateral()
K.noofsides()
 
R = Pentagon()
R.noofsides()
 
K = Hexagon()
K.noofsides()
```

Output:
```
I have 3 sides
I have 4 sides
I have 5 sides
I have 6 sides
```

Note: The “Polygon” class has an abstract method called “noofsides” that needs to be implemented by its subclasses. There are four subclasses of “Polygon” defined: “Triangle,” “Pentagon,” “Hexagon,” and “Quadrilateral.” Each of these subclasses overrides the “noofsides” method and provides its own implementation by printing the number of sides it has. In the driver code, instances of each subclass are created, and the “noofsides” method is called on each instance to display the number of sides specific to that shape.

---
*Example 02* :
```python
# Python program showing abstract base class work
from abc import ABC, abstractmethod
 
class Animal(ABC):
    def move(self):
        pass
 
class Human(Animal):
    def move(self):
        print("I can walk and run")
 
class Snake(Animal):
    def move(self):
        print("I can crawl")
 
class Dog(Animal):
    def move(self):
        print("I can bark")
 
class Lion(Animal):
    def move(self):
        print("I can roar")
 
# Driver code
R = Human()
R.move()
 
K = Snake()
K.move()
 
R = Dog()
R.move()
 
K = Lion()
K.move()
```

Output:
```
I can walk and run
I can crawl
I can bark
I can roar
```

Note: This code defines an abstract base class called “Animal” using the ABC (Abstract Base Class) module in Python. The “Animal” class has a non-abstract method called “move” that does not have any implementation. There are four subclasses of “Animal” defined: “Human,” “Snake,” “Dog,” and “Lion.” Each of these subclasses overrides the “move” method and provides its own implementation by printing a specific movement characteristic.

---
*Example - 03: Implementation of Abstract through Subclass*
```python
# Python program showing implementation of abstract class through subclassing
import abc
 
class parent:      
    def geeks(self):
        pass
 
class child(parent):
    def geeks(self):
        print("child class")
 
# Driver code
print( issubclass(child, parent))
print( isinstance(child(), parent))
```

Output:
```
True
True
```
## Inheritance:
```python
class A():
    def __init__(this):
        this.nationality="Pakistani"
        this.language='Urdu'
    
    def spaking(this, words):
        return words

class B(A):# class B extend with class A
    def eat(this,food):
        return f"Enjoying {food}"

    
qasim = B()# object

# calling
qasim.language #Output: Urdu
qasim.nationality #Output: Pakistani
qasim.spaking("Pakistan zinda bad!")  #Output: 'Pakistan zinda bad!'
qasim.eat("Biryani")  #Output:'Enjoying Biryani'
```

If another person 'aslam' is created which has the same properties as 'A' then;
```python
aslam = A()
print(aslam.nationality)
print(aslam.language)
print(aslam.spaking("Hello"))
# print(aslam.eat("Biryani")) #error
```

Output:
```
Pakistani
Urdu
Hello
```

## Poly Morphism:
## Over Riding 
```python
print(sum([7,9.2]) )#int,float
print(sum([7,2]))#int, int
```

Output:
```
16.2
9
```

## Over Loading 
```python
a = 'abc' # old value
a = 'xyz' # overload-> updated value

print(a)
```

Output:
```
xyz
```

### Examples"
*Example 01*:
```python
class A():
    def __init__(self):
        pass
    
    def my_sum(self, *num): # you can pass 1 or many numbers
        return sum(num)
    
obj1 = A()    
print(obj1.my_sum(1,2,3))
print(obj1.my_sum(1,2,3,3,5,3))
```

Output:
```
6
17
```

*Example 02*:
```python
class A():
    def __init__(self):
        print("Parent")
    
    def speaking(self): 
        print("hello I am parent...")

class B(A):
    def __init__(self): # Over Riding
        self.words=None
        print("Child")
    
    def speaking(self): #Over Riding
        print("Hello World Child..")
    
        
x1=B()# child
x1.speaking()
```

Output:
```
Child
Hello World Child..
```

## Encupsulation:
```python
class A():
    def __init__(self,name,age):
        self.__name=name # private attributes
        self.__age=age
    
    def display(self):# getter function
        return "Name is: {} {} old.".format(self.__name,self.__age)
    
    
    def setValues(self,name,age):# setter function
        self.__name=name
        self.__age=age
    
    def __hello(self):# private method
        return "Hahahahah!"

p1 = A("Osama",21)
p1.display()

# p1.name       #error
# p1.__name     #error
# p1.__hello()  #error
p1._A__name     #Output: 'Osama'
```

Output:
```
'Name is: Osama 21 old.'
```

More:
```python
p1.setValues("Ali",32)
p1.display()

# Output:
# 'Name is: Ali 32 old.'
```

## Abstract Class:
```python
from abc import ABC, abstractmethod
 
class Shape(ABC):# abstract
    def __init__(self, shape_name):
        self.shape_name = shape_name
    
    @abstractmethod
    def draw(self):
        pass
```

```python
class Circle(Shape):
    def __init__(self):
        super().__init__("circle")
 
    def draw(self):
        print("Drawing a Circle")


class Triangle(Shape):
    def __init__(self):
        super().__init__("triangle")
 
    def draw(self):
        print("Drawing a triangle")
        
# sp = Shape('shap')   #error

cr = Circle()
cr.draw() #Output: Drawing a Circle

tr = Triangle()
tr.draw()  #Output: Drawing a triangle
```
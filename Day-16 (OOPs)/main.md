## Linear Programming:
Means it prints line by line.

```python
print("line1")
print("line2")
print("line3")
print("line4")
```

Output:
```
line1
line2
line3
line4
```

## Structure Programming:
Means ut executes code in form of some statements like: with block, for loop, if/else loop

```python
for idx in range(1,5):
    print(f"line{idx}")
```

Output:
```
line1
line2
line3
line4
```

We want to manage indivdual object all methods and attributes.

```python
s1_name = "Muhammad Qasim"
s1_fname= "Muhammad Aslam"
s1_edu = "MSDS"
def s1_login():pass

s2_name = "Ali"
s2_fname = "Hamza"
s2_eud = "MS"
def s2_login():pass

s3_name = "Kashif"
s3_fname = "Hamza"
s3_eud = "MS"
def s3_login():pass
```

# OOP (Object Oriented Programming):
Class
* constructor/intializer
* Methods/Action/functions
* Attributes/properties/fields

There are four plures
* Inheritance
* Polymorphism
* Abstraction
* Encapsulation

* class: blue print
* constructor/intializer: this is also a method, call when we create new object of this class. __init__(self)

```python
class Student():
    def __init__(self): # constructor
        self.roll = None # attributes/properties
        self.name = None
        self.fname = None
        self.edu = None # attributes/properties
        
    def login(self): # method
        return f"Welcome Dear {self.name}! NED University!"
    
    def profile(self):
        return f"""
        Student Name: {self.name}
        Father's Name: {self.fname}
        Education: {self.edu}
        """

s1 = Student() # s1 object or instance of Student class
print(s1.profile())
s1.roll = 1 # update
s1.name = "Muhammad Qasim" #update
s1.fname = "Muhammad Aslam" # update
s1.edu = "MSDS"
print(s1.profile())      
```

Output:
```
        Student Name: Muhammad Qasim
        Father's Name: Muhammad Aslam
        Education: MSDS
```

```python
s1.login() #Output: 'Welcome Dear Muhammad Qasim! NED University!'
```

Now assign roll and name during initailizing the new object
```python
class Student():
    def __init__(self, roll_no, sname, fname):
        self.s_id = roll_no
        self.student_name = sname
        self.father_name = fname
        self.education = None
        self.age = None
        self.gender = None
        
    def login(self):
        return f"Welcome Dear {self.student_name} NED University!"
    
    def profile(self):
        return f"""
Student Name: {self.name}
Father's Name: {self.fname}
Education: {self.edu}
        """

s1 = Student(1,"Muhammad Qasim","Muhammad Aslam")# create new object
s2 = Student(2,"Hamza","Kashif")
s3 = Student(3,"Asif","Abid")


print(s1.login())  #method calling
print()
print(s2.login())
print()
print(s3.login())
print()
```

Output:
```
Welcome Dear M.Qasim NED University!

Welcome Dear Hamza NED University!

Welcome Dear Asif NED University!
```

## Class Varible:
```python
class Student():
    total_student = 0# class Variable
    batch = "batch-5"
    timing = "Sat and Sun"
    
    def __init__(self, roll_no, sname, fname):
        self.s_id = roll_no
        self.student_name = sname
        self.father_name = fname
        self.education = None
        self.age = None
        self.gender = None
        Student.total_student += 1 # call class variable
        
    def __del__(self):
        Student.total_student -= 1 # call class variable
        
    def login(self):
        return f"Welcome Dear {self.student_name} NED University!"
    
    def profile(self):
        return f"""
Student Name: {self.name}
Father's Name: {self.fname}
Education: {self.edu}
        """
    
print(Student.total_student) # call class variable   0   
s1 = Student(1,"Muhammad Qasim","Muhammad Aslam")# create new object 0+1=1
print(Student.total_student)  #1     
s2 = Student(2,"Hamza","Kashif")# 1 = 1+1 = 2
print(Student.total_student) # 2
s3 = Student(3,"Asif","Abid") # 2 = 2+1 = 3  
print(Student.total_student) # 3 
```

Output:
```
0
1
2
3
```

Calling class varaible for student:
```python
print(Student.batch)# class variable
print(Student.timing) # class variable
```

Output:
```
batch-5
Sat and Sun
```

Timing for each student:
```python
print(s1.timing)
print(s2.timing)
print(s3.timing)
```

Output:
```
Sat and Sun
Sat and Sun
Sat and Sun
```

To delete s1:
```python
del s1
```

Total number of students:
```python
Student.total_student #output: 3
```
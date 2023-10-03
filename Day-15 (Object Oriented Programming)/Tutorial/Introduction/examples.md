## Examples:

Below is the way by which we created class and constructor in old languages.
```python
class Student():
    def Student(self):# old programming/java/dotnet constructor
        print("hello")
            
s1 = Student()
```

### Create a system of a student for fee submission.
* Without __init__() Function:
```python
class Student():
    def Student(self):  # constructor/intializer
        print("I'm constructor function")
        
    def admission(self): # method
        print("Admission has been done")
        
    def pay_fee(self):  # method
        print("Fee has been submitted")
        
        
kamran = Student() #object

# calling a class function/method
kamran.admission() 
kamran.pay_fee()
```

Output:
```
Admission has been done
Fee has been submitted
```

* With __init__() Function:
```python
class Student():
    def __init__(self):   # constructor/intializer 
        print("I'm constructor function")  #init() use to call function itself
        
    def admission(self): #method
        print("Admission has been done")
        
    def pay_fee(self):#method
        print("Fee has been submitted")
        
        
kamran = Student() #object

# calling a class function/method
kamran.admission()
kamran.pay_fee()
```

Output:
```
I'm constructor function
Admission has been done
Fee has been submitted
```

## Use of Attribute in class:
* When we don't provide any value of student => means no argumengts provided
```python
class Student():
    def __init__(self):  # constructor/intializer 
        self.name = None # attribute
        self.father_name = None # attribute
        self.age = None # attribute
        self.roll_no = None# attribute
        
    def admision(self):
        print("Admision completed")
    
    def student_details(self):
        data = f"""
        Student Name: {self.name}
        Student Father's Name {self.father_name}
        Roll no: {self.roll_no}
        """
        print(data)
        
s1 = Student()
s1.student_details()

s2 = Student()
s2.student_details()
```

Output:
```
        Student Name: None
        Student Father's Name None
        Roll no: None
        

        Student Name: None
        Student Father's Name None
        Roll no: None
```

* Pass argments during creating object:
```python
class Student():
    def __init__(self, sname, rollno):  # constructor/intializer
        self.name = sname # attribute
        self.father_name = None # attribute
        self.age = None # attribute
        self.roll_no = rollno # attribute
        
    def admision(self):
        print("Admision completed")
    
    def student_details(self):
        data = f"""
        Student Name: {self.name}
        Student Father's Name {self.father_name}
        Roll no: {self.roll_no}
        """
        print(data)
        
s1 = Student("kamran",1)
s1.student_details()

s2 = Student("Amir",2)
s2.student_details()
```

Output:
```
        Student Name: kamran
        Student Father's Name None
        Roll no: 1
        

        Student Name: Amir
        Student Father's Name None
        Roll no: 2
```
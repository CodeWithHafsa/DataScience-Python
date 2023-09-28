## Create Own Error:

* First Create a function:
```python
class StudentCard():
    def __init__(self, roll, name, age):
        if age < 18 or age > 60:
            raise Exception("Not allowed less 18 or graterthan 60 years")
        self.roll = roll
        self.name = name
        self.age = age
```
---
* Then if input = is not less than 18 or more than 60 (means no error raise.)
```python
s1 = StudentCard(1,'Muhammad Qasim', 29)
print(s1.name)
print(s1.roll)
print(s1.age)
```

Output:
```
Muhammad Qasim
1
29
```
---
* But if input = is less than 18 or more than 60 (means error raise.)
```python
try:
    s1 = StudentCard(1,'Muhammad Qasim', 10) #error
except Exception as e:  #errorclass exception
    print(e) #error raise
``` 

Output:
```
Not allowed less 18 or graterthan 60 years
```

## To change class of Error - along with message:

```python
class StudentCard():
    def __init__(self, roll, name, age):
        if age < 18 or age > 60:
            raise StudentAgeError("Not allowed less 18 or graterthan 60 years")
        self.roll = roll
        self.name = name
        self.age = age
        
class StudentAgeError(Exception):  #error class = StudentAgeError
    pass

print("Start Line")
try: 
    l1= [1,3,3,3]
    print(l1[2])
    s1 = StudentCard(1,'Muhammad Qasim', 12)
except Exception as e:
    print("Error Reason!...",e)
    
print("End line")
```

Output:
```
Start Line
3
Error Reason!... Not allowed less 18 or graterthan 60 years
End line
```

---
* To check class, write:
```python
s1 = StudentCard(1,'Muhammad Qasim', 12)
```

Output:
```
--- StudentAgeError: Not allowed less 18 or graterthan 60 years ---
```
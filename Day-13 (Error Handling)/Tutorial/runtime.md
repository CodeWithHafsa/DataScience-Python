## Run Time Error:
There are three steps to solve run time error:
* The `try` block lets you test a block of code for errors.
* The `except` block lets you handle the error.
* The `finally` block lets you execute code, regardless of the result of the try- and except blocks.

```
try :
    logic  #may be error accure here
except (ErrorClass1, ErrorClass2):
    action
else:
    run if error not accure
finally:
    line always run
```
---

*Example 01 - Handling Name Error*:
```python
print("line1")
print("line2")

try:
    print(a)
except NameError:
    print("Variable is not define!")

print("line4")
print("line5")
```

Output:
```
line1
line2
Variable is not define!
line4
line5
```

=========================================================
*Example 02 - Handling Zero Division Error* :
```python
print("line1")
print("line2")

num1 = 7
num2 = 0

try:
    print(num1 / num2)
except ZeroDivisionError:
    print("Variable is not define!")

print("line4")
print("line5")
```

Output:
```
line1
line2
Variable is not define!
line4
line5
```
=========================================================
*Example 03 - Handling Name Error & Zero Division Error* :
```python
print("line1")
print("line2")

num1 = 7
num2 = 0

try:
    print(b)
    print(num1 / num2)
except (ZeroDivisionError, NameError):
    print("Something is wrong!")

print("line4")
print("line5")
```

Output:
```
line1
line2
Something is wrong!
line4
line5
```

=========================================================
*Example 04* :
There are three logics in the below example - jo logic sabsy pehley ghalat hogi python uska error dega or baqi 2 ghalat logics ka error nahi deyga.

```python
print("line1")
print("line2")

num1 = 7
num2 = 0
b = 20
l = [1,2,3,3,5,6,7]

try:
    print(b)   #logic1
    print(num1 / num2)    #logic2
    print('hello')
    print(l[20])   #logic3
    print("world")
except (ZeroDivisionError, NameError):
    print("Something is wrong!")

print("line4")
print("line5")
```

Output:
```
line1
line2
Name Error
line4
line5
```

* If we want to create an error for every wrong logic case, we have to wrte 'try-except' for evert logic, as shown below:
```python
print("line1")
print("line2")

num1 = 7
num2 = 0
b = 20
l = [1,2,3,3,5,6,7]

try:
    print(d)# logic
except (NameError):
    print("Name Error")
      
try:
    print(num1 / num2)# right code logic
except (ZeroDivisionError):
    print("Zerro Error")
      
print('hello')

try:
    print(l[20]) # logic3
except (IndexError):
    print("Index Error")
      
print("world")
```

Output:
```
line1
line2
Name Error
Zerro Error
hello
Index Error
world
```

### Dynamically Handling:
If we don't want to write 'try-except' logic for every wrong case, we can also handle it dynamically but using `exception`.

*Example* :
```python
print("line1")
print("line2")

num1 = 7
num2 = 2
b = 20
l = [1,2,3,3,5,6,7]

try:
    print(b)# logic1
    print(num1 / num2) # logic2
    print('hello')
    print(l[20]) # logic3
    print("world")
except Exception as e:   #here e - tells 'type of error'
    print(f"Something is wrong! {e}")

print("line4")
print("line5")
```

Output:
```
line1
line2
20
3.5
hello
Something is wrong! list index out of range
line4
line5
```
# Error Handling:
It is also knwon as 'Exception Handling'.
When an error occurs, or exception as we call it, Python will normally stop and generate an error message.

There are three types of errors:
* Development time error - It means there is error in coding.
* Logical error - It means operation doesnot perform according to logics and error generate. It can be check via. dry run testing (step by step testing)
* Run time error - Runtime errors are commonly called referred to as “bugs”. It means error in server/application. It is an error that occurs while the program is running after being successfully compiled.

## Development Time Error:
It means there is error in coding.

*Example 01* :

* It prints line1 and line 2, after that it shows error because in third line their is not defined value of 'a'. 
```python
print("line1")
print("line2")
print(a)     #create error 
print("line4")
print("line5")
```

Output:
```
line1
line2
----- NameError ----
```

* To solve error, define value of a = 'Python'
```python
a = "Python"
print("line1")
print("line2")
print(a)
print("line4")
print("line5")
```

Output:
```
line1
line2
Python
line4
line5
```

* It prints line1 and line2, but doesnot print line3 because the value of b defined at last, it should be at first.
```python
print("line1")
print("line2")
print(b)    #create error
print("line4")
print("line5")
b = "Pakistan"
```

Output:
```
line1
line2
----- NameError ----
```
=========================================================
*Example 02* :
* `TypeError` cause - because one number is 'string' and another one is 'integar'.

```python
2 + "2"   
```

Output:
```
----- TypeError ------
```

=========================================================
*Example 03* :
* `IndexError` cause - because at index[7] there is no number present in the list.
```python
l = [1,2,2,4]
print(l[7])
```

Output:
```
----- IndexError ----
```
=========================================================
*Example 04* :

* `TypeError` cause - because tuple is immutable. 
```python
a = (1,23,2)
a[0] = 200
```

Output:
```
----- TypeError -----
```
=========================================================
*Example 05* :

* `ZeroDivisionError` cause - because 7/0 = infinity. 
```python
7 / 0
```

Output:
```
------ ZeroDivisionError ------
```
=========================================================
*Example 06* :

* `FileNotFoundError` cause - file is not present in the folder. 
```python
open("abc.txt")
```

Output:
```
--------- FileNotFoundError -------
```


## Logical Error:
It means operation doesnot perform according to logics and error generate. It can be check via. dry run testing (step by step testing).

*Example*:

In the below example, we created a function two add two numbers but in logic instead of a+b ---> we write a-b, that's why instead of adding the two numbers subtracted.

```python
def add_two_nums(a,b):
#     print(a,b, type(a),type(b))
    return a - b

add_two_nums(7,7)  # create case 7+7 = 14 Flse
```

Output:
```
0
```
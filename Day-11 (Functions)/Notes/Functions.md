# Functions:
A function is a block of code which only runs when it is called.\
You can pass data, known as parameters, into a function.\
A function can return data as a result.

There are two types of functions:
1. Pre-defined functions  - These are built into the software and does not need to be created by a programmer i.e. provided by community.
* Pre-defined functions are also known as 'default function'.\
E.g. print, len, str etc.
2. User-defined functions - These are custome function created by programmer(you).

There are two types of functions: Return function and Non-return function:
* Return statement - is a special statement that you can use inside a function or method to send the function's result back to the caller. A return statement consists of the return keyword followed by an optional return value.
* Non- return function - is a function without an explicit return statement returns None. Non-return functions like this are called void, and they return None, Python's special object for "nothing".

Some common properties in a function are:
* Return statement
* Non-return statement
* Required-parameters
* Optional parameters
* Defualt function
* Postional argument
* Key value parameters
* Pass ulimited optional argument
* Pass ulimited key=value argument

Steps of functions:

* Creating a function:
In Python a function is defined using the def keyword:

```python
def my_function():  # function declaration/signature
  print("Hello from a function")
```

* Calling a function:
To call a function, use the function name followed by parenthesis:
``` python
def my_function():   # function declaration/signature
  print("Hello from a function")   #fucntion body

my_function()
```

## Reserved Keywords:
|     Keyword         |             Description                  |
|---------------------| -----------------------------------------|
|         `and`       |       A logical operator                 |
|         `as`        |       To create an alias                 |
|       `assert`      |       For debugging                      |
|        `break`      |       To break out of a loop             |
|        `class`      |       To define a class                  |
|       `continue`    |       To continue to the next iteration of a loop                  |
|       `def`         |       To define a function               |
|       `del`         |       To delete an object                |
|       `elif`        |      Used in conditional statements, same as else if                |
|       `else`        |      Used in conditional statements      |
|       `except`      |      Used with exceptions, what to do when an  exception occurs      |
|       `False`       |      Boolean value, result of comparison operations      |
|       `False`       |      Boolean value, result of comparison operations finally	Used with exceptions, a block of code that will be executed no matter if there is an exception or not    |
|       `for`        |      To create a for loop             |
|       `from`        |     To import specific parts of a module             |
|       `global`    |     To declare a global variable                |
|       `if`        |     To make a conditional statement             |
|       `import`        |     To import a module             |
|       `in`        |     To check if a value is present in a list, tuple, etc.             |
|       `is`        |     To test if two variables are equal.             |
|       `lambda`      |     To create an anonymous function             |
|       `None`        |     Represents a null value                     |
|       `nonlocal`        |     To declare a non-local variable                     |
|       `not`        |     A logical operator                     |
|       `or`         |     A logical operator                     |
|       `pass`       |     A null statement, a statement that will do nothing                     |
|       `raise`       |     To raise an exception                     |
|       `return`      |    To exit a function and return a value                     |
|       `True`      |   Boolean value, result of comparison operations try	To make a try...except statement                     |
|       `while`      |   To create a while loop                    |
|       `with`       |   Used to simplify exception handling                    |
|       `yield`       |   To end a function, returns a generator                    |


## Example of Non-Return Funtion:
Non - return function - is a function without an explicit return statement returns None. 

*Example* :
```python
def introduction():         #Signature/function decrairlation
    print("NED University") #body start
    print("PGD Data Science - Generative AI Program!")
    print("Batch 5")
    print("Saturday & Sunday Calsses")  #body end

abc = introduction()   # function calling
print(abc)   #here function doesnot use return keyword, so it does not return any value in print(abc)
```

Output:
```
NED University  #output of abc = introduction() 
PGD Data Science - Generative AI Program!
Batch 5
Saturday & Sunday Calsses
None  #output of print(abc)
```

As many times you call the function, as many times the result prints. 

## Example of Return Funtion:
Return statement is a special statement that you can use inside a function or method to send the function's result back to the caller. A return statement consists of the return keyword followed by an optional return value.

*Example* :
```python
def introduction():# Signature/function decrairlation
    print("NED University") # body start
    print("PGD Data Science - Generative AI Program!")
    print("Batch 5")
    print("Saturday & Sunday Calsses") # body end
    
    return "Python Function!"  #return statement

abc = introduction()  # function calling
print(abc)
```

Output:
```
NED University
PGD Data Science - Generative AI Program!
Batch 5
Saturday & Sunday Calsses
Python Function!
```

* We can return multiple data types in one function - known as 'multireturn function':
```python
def introduction(): #Signature/function decrairlation
                    #no body inside function
    return "Pakistan zinda bad!", 123, 'xyz' #multireturn 

abc = introduction()# function calling
print(abc)
```

Ouput:
```
('Pakistan zinda bad!', 123, 'xyz')
```

## Some Information:
* pypi.org - to create packages in python.
* quivr github - to create applications.
* typescript - coding language.
* seamless m4t meta - is a translator platform on hugging face. 

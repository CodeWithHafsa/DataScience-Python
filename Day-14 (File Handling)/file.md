# File Handling:
File handling in Python is a powerful and versatile tool that can be used to perform a wide range of operations.

## Python open() Function:
The open() function opens a file, and returns it as a file object. Read more about file handling in our chapters about File Handling.

### Syntax:
```
open(file, mode) 
```

### Parameter Values:
* file ----> The path and name of the file
* mode ----> A string, define which mode you want to open the file in: (`r, a, w, x`) 
* Works according to UTF-8 standards.
---

#### Here:

|    Word   |     Name                 |        Description      |
|-----------|--------------------------|-------------------------|
|`r`|Read - Default value        | Opens a file for reading, error if the file does not exist|
|`a`|Append | Opens a file for appending, creates the file if it does not exist|
|`w`|Write | Opens a file for writing, creates the file if it does not exist|
|`x`|Create | Creates the specified file, returns an error if the file exist|

In addition you can specify if the file should be handled as binary or text mode:
* `t` -----  Text - Default value. ---- Text mode
* `b` -----  Binary ---- Binary mode (e.g. images)

## Examples - Using File Mode:
* If we use open command, to read or write the file then we have to close it using `f.close()`
* If we use `with` block with open function then we don't need to close the file, it will close automatically.

## PYTHON READ FILES:
### - Read Only:
*Example* :
```python
f = open("abc.txt")
print(f.read())  #read file
f.close()
```

Output:
```
Hello
Welcome to Python Learning 
Day-14
```
---
### Read Only Parts of the File:
*Example* :
```python
f = open("demofile.txt", "r")
print(f.read(5))   #returns the 5 first characters of the file
```

Output:
```
Hello
```
---
### - Readline or  Readlines:
*Example 01 - Readline* :

```python
f = open("abc.txt")
print(f.readline()) #using readline: it prints only first line of the file
f.close()
```

Output:
```
Hello
```
========================================================
*Example 02 - Readline* :

```python
f = open("abc.txt")
print(f.readline()) #using readline: it prints only first line of the file
print(f.readline()) #using readline: it prints second  line of the file
f.close()
```

Output:
```
Hello
Welcome to Python Learning 
```
========================================================
*Example 03 - Readlines* :

```python
f = open("abc.txt")
print(f.readlines()) #using readlines: it prints all lines in one line using \n. 
f.close()
```

Output:
```
['Hello\n', 'Welcome to Python Learning\n', 'Day-14']
```
========================================================
*Example 04 - list* :

```python
list(open('abc.txt'))  #list also do same work as readlines.
```

Output:
```
['Hello\n', 'Welcome to Python Learning\n', 'Day-14']
```
---
### - Loop:
The read mode within a loop:

```python
f = open("abc.txt", "r")
for x in f:
  print(x)
```

Output:
```
Hello

Welcome to Python Learning

Day-14
```

## PYTHON WRITE FILES:
To write to an existing file, you must add a parameter to the open() function:
* "a" - Append - will append to the end of the file
* "w" - Write - will overwrite any existing content

Note: In write method, if there is no file of given name in the folder, then it will automatically create a file of given name. 

### - Write mode with append
The write mode with append - adds the new line in the previous file as shown below:

```python
f = open("demofile2.txt", "a")  # a= appned
f.write("Now the file has more content!")
f.close()

#open and read the file after the appending:
f = open("demofile2.txt", "r")
print(f.read())
``` 

Output:
```
Hello! Welcome to demofile2.txt
This file is for testing purposes.
Good Luck!Now the file has more content!
```
---
### Overwrite:
The write mode only - overwrite the text in the file, means it delete all the previous text and only add the new text provided by the user as shown below:

```python
f = open("demofile3.txt", "w")   #w = overwrite the txt present in file.
f.write("I have deleted the content!")
f.close()

#open and read the file after the overwriting:
f = open("demofile3.txt", "r")
print(f.read())
```

Output:
```
I have deleted the content!
```

## Create a New File IN PYTHON:
To create a new file in Python, use the open() method, with one of the following parameters:
* "x" - Create - will create a file, returns an error if the file exist
* "a" - Append - will create a file if the specified file does not exist
* "w" - Write - will create a file if the specified file does not exist

### - Create file:

```python
f = open("myfile.txt", "x")  # x= create an empty error file
```

Output:
```
a new empty file is created!
```
---
### - Create a new file if it doesnot exist
```python
f = open("myfile.txt", "w")
```

## PYTHON DELETE FILES:
To delete a file, you must import the OS module, and run its os.remove() function:

### - Delete file:
Remove the file "demofile.txt":
```python
import os
os.remove("demofile.txt")
```
---
### - Check if File exist:
To avoid getting an error, you might want to check if the file exists before you try to delete it:

```python
import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist")
```

## Delete Folder:
To delete an entire folder, use the os.rmdir() method:
```python
import os
os.rmdir("myfolder")
```
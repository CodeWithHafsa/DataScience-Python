## Use of with block:
If we use `with` block with open function then we don't need to close the file, it will close automatically.

```python
with open("./abc.txt") as file:  #./abc.txt = relative path
    a = file.readlines()
    print(a)
```

Output:
```
['Hello\n', 'Welcome to Python Learning\n', 'Day-14']
```

## Examples Using File Modes:
Below are some examples using with block and different file modes:

## Read Only :
*Example 01* :
```python
with open("./abc.txt", mode='r') as file:   # mode r = read
    a = file.readlines()  #readlines
    print(a)
```

Output:
```
['Hello\n', 'Welcome to Python Learning\n', 'Day-14']
```
========================================================
*Example 02* :
```python
f = open("abc.txt", "r")
print(f.read(5)) #printsonly first 5 characters
```

Output:
```
Hello
```

## Readlines with slicing:
```python
# with open(file) as <variable>
with open("file.txt") as file:
    content = file.readlines()[:3] #read line have index 0 to 3
    print(type(content))
    print(content)
```

Output:
```
<class 'list'>
['Hello Welcome\n', 'New line1\n', 'New line2\n']
```

## Write Only:

```python
with open("./abc.txt", mode='w') as file:  #mode w = write
    file.write("aaaaa")   #write "aaaaa" in the text file   
``` 

Output:
```
aaaaa     #in abc.txt file
```

## Read and Write:
There are two modes to read and write both:
* r+ = read plus write
* w+ = write plus read

*Example* :
```python
with open("demofile.txt", mode='r+') as file: # r+ = read and write
    a = file.readlines() # read file here
    print(a)
    file.write("\nHello world!")
    file.seek(0)   #seek - to move indentation(cursor) to zero
    a = file.readlines() # read file here
    print(a)
```

Output:
```
['Hello\n', 'Welcome to Python Learning\n', 'Day-14']
['Hello\n', 'Welcome to Python Learning\n', 'Day-14\n', 'Hello World']
```

## Append mode:
Append mode - it creates a new file with the given text.

```python
with open("xyz.txt", 'a+') as f:
    f.write("\nHello world")
    f.seek(0)         #seek - to move indentation(cursor) to zero
    print(f.read())   #read
```

Output:
```

Hello world
```

# To read a image: 
```python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg

img=mpimg.imread('./files/a.jpg')   # read image
# print(img.shape)#
plt.imshow(img)   #display image
```

## Some Points:
* To read an image - use matplotlib or opencv
* To read a video - use opencv
* To read a audio file - import matplotlib.pyplot as plt, import numpy as np, import wave, import sys
## Path in File Handling:
There are two types of paths:
1. Absolute path 
2. Relative path  

## 1. Absolute Path:
An absolute file path describes how to access a given file or directory, starting from the root of the file system. A file path is also called a pathname. 

Example:
```python
/Users/Desktop/Python/Day-14/abc.txt #complete path
```

## 2. Relative Path:
Relative file paths are notated by a lack of a leading forward slash. A relative file path is interpreted from the perspective your current working directory. 

Example: 
```python
./                 #current location
./xyz/aa/xyz.txt   #current location + next folders
../                # /Users/Desktop/Python/Day-14/ (current location + one previous folders)
../../             # /Users/Desktop/Python/ (current location + two previous folders)
```


## Key Points
* pwd (The password database) -----> This module provides access to the Unix user account and password database. It is available on all Unix versions.
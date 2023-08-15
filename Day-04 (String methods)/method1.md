# String Methods
All methods/function, attributes/properties/fields of string - can be determined using 'dir' function.

### 1. capitalize()
The capitalize() method - Turns only the first character of the string to uppercase and the rest other characters of the string are turned to lowercase. 

The string has no effect if the first character is already uppercase.

*Example:*
```python
text = """pyThon LAnguAge!
IntroduCtion to Python."""
print(text.capitalize()) #turns only the first character of the string to uppercase.
```

Output:
```markup
Python language!       
introduction to python.
```
_____

### 2. casefold() 
The casefold() method - Converts string into lower case. 

*Example*
```python
text = """pyThon LAnguAge!
IntroduCtion to Python."""
print(text.casefold()) #converts string into lower case.
```

Output:
```markup
python language!       
introduction to python.
```
_____

### 3. center()
The center() method - Returns a centered string.

*Example*

```python
name = "Hafsa Imtiaz"
name.center(20) #center string - overall len=20.
```

Output:
```markup
'    Hafsa Imtiaz    '
```
___

### len()
The len() method / _len_() method - use to determine length of a string including space.

*Example*

```python
name = "Hafsa Imtiaz"
print(len(name)) #method #global len function
#or #print(name._len_())
```

Output:
```markup
12
```
___

### 4. count()
The count() method - Returns the number of times the given value has occurred within the given string.

*Example#1*

```python
name = "Hafsa Imtiaz"
name.count("a") #it counts that how many times a present in a string.
```

Output:
```markup
3
```
___
*Example#2*

```python
name = "Muhammad Qasim is teaching AI in NED."
name.count("Qasim") 
```

Output:
```markup
1
```
___
*Example#3*

```python
name = "Muhammad Qasim"
print(name.count("m") + name.count("a"))
```

How it works:
```
Count m: 3
Count a: 3
      m + a = 3 + 3 = 6
```

Output:
```markup
6
```
___
*Example#4*

```python
name = "Muhammad Qasim"
print(name.count("m") + name.count("a") + name.count("M") + name.count("A"))
```

How it works:
```
Count m: 3
Count a: 3
Count M: 1
Count A: 0
      m + a + M + A = 3 + 3 + 1 + 0 = 7
```

Output:
```markup
7
```
___
*Example#5*

```python
name = "Muhammad Qasim"
name = name.casefold() #it converts all letters into small alphabets.
print(name.count("m") + name.count("a")) #count m and a
```

Output:
```markup
7
```
___
### 4. encode()
The encode() method - Returns an encoded version of the string. 

*Example#1*

```python
txt = "My name is Ståle"
x = txt.encode() #encode ' å ' acccording to utf-8 standards
print(x)
```

Output:
```markup
b'My name is St\xc3\xa5le'
```
---
*Example#2*

```python
txt = "My name is Ståle"

print(txt.encode(encoding="ascii",errors="backslashreplace"))
print(txt.encode(encoding="ascii",errors="ignore"))
print(txt.encode(encoding="ascii",errors="namereplace"))
print(txt.encode(encoding="ascii",errors="replace"))
print(txt.encode(encoding="ascii",errors="xmlcharrefreplace"))
```

Output:
```markup
b'My name is St\\xe5le'
b'My name is Stle'
b'My name is St\\N{LATIN SMALL LETTER A WITH RING ABOVE}le'
b'My name is St?le'
b'My name is St&#229;le'
```
___
### 5. endswith():
The endswith() method -  checks if the string ends with a given value. If yes then return True, else return False.

*Example*

```python
name = "Muhammad Qasim"
print(name.endswith("m")) #check if given value endswith 'm'
print(name.endswith("sim")) #check if given value endsith 'sim'
```

Output:
```markup
True
True
```
---

### 6. startswith():
The endswith() method -  checks if the string starts with a given value. If yes then return True, else return False.

*Example#1*

```python
name = "Muhammad Qasim"
print(name.startswith("M")) #check if given value startswith 'M'
print(name.startswith("sim")) #check if given value startswith 'sim'
```

Output:
```markup
True
False
```
---
*Example#2*

```python
name = "Muhammad Qasim"
search = input("start with ")
print(name.startswith(search)) #check if the value given by user startswith in the given string
print(name.startswith("sim")) #check if given value startswith 'sim'
```

Output:
```markup
True
False
```
___
### 7. expandtabs():
The expandtabs() method - Sets the tab size of the string (i.e. it create string of given size).

*Example*

```python
card = """
NED University
Batch5
Class:\tPython
Name:\tHafsa Imtiaz
Father's Name:\t Imtiaz Ahmed
"""
print(card.expandtabs(10)) #len of string=10 including space
print(card.expandtabs(30)) #len of string=30 including space
```

Output:
```markup
NED University
Batch5
Class:    Python
Name:     Hafsa Imtiaz
Father's Name:      Imtiaz Ahmed


NED University
Batch5
Class:                        Python
Name:                         Hafsa Imtiaz
Father's Name:                Imtiaz Ahmed
```
---
### 8. lower():
The lower() method - Converts a string into lower case.

*Example*

```python
name = "MuHaMmad QaSiM"
print(name.lower())
```

Output:
```markup
muhammad qasim
```
---
### 9. lstrip():
The lstrip() method - Returns a left trim version of the string / removes trailing characters (!!!) that are at the start of string.

*Example*
```python
name = "    Muhammad Qasim"
name.lstrip() #removes characters that are at the start of string.
```

Output:
```markup
'Muhammad Qasim'
```
### 10. rstrip():
The rstrip() method - Returns a right trim version of the string / removes trailing characters (!!!) that are at the end of string.

*Example*
```python
name = "Muhammad Qasim   "
name.rstrip() #removes characters that are at the end of string.
```

Output:
```markup
'Muhammad Qasim'
```

### 11. strip():
The strip() method - Returns a trimmed version of the string /  removes trailing characters (!!!) that are at the start and end of string. But it doesnot remove in between characters or space.

*Example*
```python
name = "    Muhammad       Qasim   "
name.strip() #removes characters at the start and end of string.
```

Output:
```markup
'Muhammad       Qasim'
```
___
### 12. replace():
The replace() method - Returns a string where a previous given value is replaced with a  new given value.

*Example#1*
```python
name = "Muhammad Qasim"
name.replace("Qasim", "Aslam")
```

Output:
```markup
'Muhammad Aslam'
```

*Example#2*
```python
name = "Muhammad Qasim Qasim Qasim"
name.replace("Qasim","Aslam", 1) #replace only 1st index of string.
```

Output:
```markup
'Muhammad Aslam Qasim Qasim'
```

*Example#3*
```python
name = "Muhammad Qasim Qasim Qasim"
name.replace("Qasim","Aslam", -1) #replace all index of string.
```

Output:
```markup
'Muhammad Aslam Aslam Aslam'
```
___
### 13. index():
The index() method - Searches the string for a given value and returns the position of where it was found.

*Example*
```python
name = "Muhammad Qasim Qasim Qasim"
name.index("Qasim")
```

Output:
```markup
9
```
___
### 14. find():
The find() method - Searches the string for a given value and returns the position of where it was found.

*Example*
```python
name = "Muhammad Qasim Qasim Qasim"
name.index("Qasim", 16) #tells index after 16 - where given value present.
```

Output:
```markup
21
```
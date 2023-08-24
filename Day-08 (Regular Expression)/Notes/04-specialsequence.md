# Special Sequences
Special sequences make commonly used patterns easier to write.

A special sequence is a \ followed by one of the characters in the list below, and has a special meaning:
|   Character             |Description                           |             
|----------------|-------------------------------|
| \A | Returns a match if the specified characters are at the beginning of the string          |
| \b | Returns a match where the specified characters are at the beginning or at the end of a word. (Use "r")          |
| \B | Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word. (Use "r")     |
| \d | Returns a match where the string contains digits (numbers from 0-9)         |
| \D | Returns a match where the string DOES NOT contain digits        |
| \s | Returns a match where the string contains a white space character       |
| \S | Returns a match where the string DOES NOT contain a white space character       |
| \w | Returns a match where the string contains any word characters (characters from a to Z, digits from 0-9, and the underscore _ character)       |
| \W | Returns a match where the string DOES NOT contain any word characters       |
| \Z | Returns a match if the specified characters are at the end of the string       |

* With \b or With \B - the "r" in the beginning is making sure that the string is being treated as a "raw string"

## 1. \A - Matches if the specified characters are at the start of a string.
*Example* :
```python
import re
txt = "The rain in Spain"

#Check if the string starts with "The":
x = re.findall("\AThe", txt)
print(x)

if x:
  print("Yes, there is a match!")
else:
  print("No match")
```

Output:
```
['The']
Yes, there is a match!
```

## 2. \b - Matches if the specified characters are at the beginning or end of a word.
* When \b - Use at the begining

*Example* :
```python
import re
txt = "The rain in Spain"

#Check if "ain" is present at the beginning of a WORD:
x = re.findall(r"\bain", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
[]
No match
```
=========================================================
* When \b - Use at the end

*Example* :
```python
import re
txt = "The rain in Spain"

#Check if "ain" is present at the end of a WORD:
x = re.findall(r"ain\b", txt) 
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
['ain', 'ain']
Yes, there is at least one match!
```

## 3. \B - Opposite of \b. Matches if the specified characters are not at the beginning or end of a word.
* When \b - Use at the begining

*Example* :
```python
import re
txt = "The rain in Spain"

#Check if "ain" is present, but NOT at the beginning of a word:
x = re.findall(r"\Bain", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
['ain', 'ain']
Yes, there is at least one match!
```
=========================================================
* When \b - Use at the end

*Example* :
```python
import re
txt = "The rain in Spain"

#Check if "ain" is present, but NOT at the end of a word:
x = re.findall(r"ain\B", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
[]
No match
```

## 4. \d - Matches any decimal digit. Equivalent to [0-9]

*Example 01* :
```python
import re
txt = "The rain in Spain"

#Check if the string contains any digits (numbers from 0-9):
x = re.findall("\d", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
[]
No match
```

=========================================================
*Example 02* :
```python
import re
text = "12abc3"

#Check if the string contains any digits (numbers from 0-9):
x = re.findall("\d", text)
print(x)
```

Output:
```
['1', '2', '3']
```

## 5. \D - Matches any non-decimal digit. Equivalent to [^0-9]
*Example 01* :
```python
import re
txt = "Rain in Spain"

#Return a match at every no-digit character:
x = re.findall("\D", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
['R', 'a', 'i', 'n', ' ', 'i', 'n', ' ', 'S', 'p', 'a', 'i', 'n']
Yes, there is at least one match!
```
=========================================================
*Example 02* :
```python
import re
text = "1ab34'50"

#Return a match at every no-digit character:
x = re.findall("\D", text)
print(x)
```

Output:
```
['a', 'b', "'"]
```

## 6. \s - Matches where a string contains any whitespace character. Equivalent to [ \t\n\r\f\v].
*Example 01* :
```python
import re
txt = "The rain in Spain"

#Return a match at every white-space character:
x = re.findall("\s", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
[' ', ' ', ' ']
Yes, there is at least one match!
```
=========================================================
*Example 02* :
```python
import re
text = "Python RegEx"

#Return a match at every white-space character:
x = re.findall("\s", text)
print(x)
```

Output:
```
[' ']
```

## 7. \S - Matches where a string contains any non-whitespace character. Equivalent to [^ \t\n\r\f\v].
*Example 01* :
```python
import re
txt = "Rain in Spain"

#Return a match at every NON white-space character:
x = re.findall("\S", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
['R', 'a', 'i', 'n', 'i', 'n', 'S', 'p', 'a', 'i', 'n']
Yes, there is at least one match!
```
=========================================================
*Example 02* :
```python
import re
text = "a b"

#Return a match at every NON white-space character:
x = re.findall("\S", text)
print(x)
```

Output:
```
['a', 'b']
```

## 8. \w - Matches any alphanumeric character (digits and alphabets). Equivalent to [a-zA-Z0-9_]. Underscore _ is also considered an alphanumeric character.
*Example 01* :
```python
import re
txt = "Rain in Spain"

#Return a match at every word character (characters from a to Z, digits from 0-9, and the underscore _ character):
x = re.findall("\w", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
['R', 'a', 'i', 'n', 'i', 'n', 'S', 'p', 'a', 'i', 'n']
Yes, there is at least one match!
```
=========================================================
*Example 02* :
```python
import re
txt = "12&': ;c "

#Return a match at every word character (characters from a to Z, digits from 0-9, and the underscore _ character):
x = re.findall("\w", txt)
print(x)
```

Output:
```
['1', '2', 'c']
```

## 9. \W - Matches any non-alphanumeric character. Equivalent to [^a-zA-Z0-9_]
*Example 01* :
```python
import re
txt = "The rain in Spain"

#Return a match at every NON word character (characters NOT between a and Z. Like "!", "?" white-space etc.):
x = re.findall("\W", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
[' ', ' ', ' ']
Yes, there is at least one match!
```

## 10. \Z - Matches if the specified characters are at the end of a string.
*Example 01* :
```python
import re
txt = "The rain in Spain"

#Check if the string ends with "Spain":
x = re.findall("Spain\Z", txt)
print(x)

if x:
  print("Yes, there is a match!")
else:
  print("No match")
```

Output:
```
['Spain']
Yes, there is a match!
```
=========================================================
*Example 02* :
```python
import re
txt = "I like Python Programming"

#Check if the string ends with "Python":
x = re.findall("Python\Z", txt)
print(x)
```

Output:
```
[]
```
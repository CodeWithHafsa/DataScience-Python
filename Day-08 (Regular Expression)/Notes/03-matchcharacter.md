# MetaCharacters
Metacharacters are characters that are interpreted in a special way by a RegEx engine.

Here's a list of metacharacters:\
`[] . ^ $ * + ? {} () \ |`


|   Character             |Description                           |             
|----------------|-------------------------------|
| [ ] | 	A set of characters           |
| \ | Signals a special sequence (can also be used to escape special characters)           |
| . | Any character (except newline character)           |
| ^ | Starts with         |
| $ | Ends with        |
| * | Zero or more occurrences       |
| + | One or more occurrences       |
| ? | Zero or one occurrences       |
| { } | Exactly the specified number of occurrences       |
| \| | Either or       |
| ( ) | Capture and group       |


## 1. `[ ]` - Square brackets :
Square brackets specifies a set of characters you wish to match.

You can also specify a range of characters using - inside square brackets.
```
[a-e] is the same as [abcde].
[1-4] is the same as [1234].
[0-39] is the same as [012 to 39].
```
You can complement (invert) the character set by using caret ^ symbol at the start of a square-bracket.
```
[^abc] means any character except a or b or c.
[^0-9] means any non-digit character.
```
---
*Example* :
```python
import re

txt = "The rain in Spain"

#Find all lower case characters alphabetically between "a" and "m":
x = re.findall("[a-m]", txt)
print(x)
```

Output:
```
['h', 'e', 'a', 'i', 'i', 'a', 'i']
```
## 2. `\` - Backslash :
Backlash \ is used to escape various characters including all metacharacters.\
Signals a special sequence (can also be used to escape special characters)

*Example* :
```python
import re

txt = "That will be 59 dollars"

#Find all digit characters:
x = re.findall("\d", txt)
print(x)
```

Output:
```
['5', '9']
```

## 3 `.` - Dot:
A period matches any single character (except newline \n).

*Example* :
```python
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by two (any) characters, and an "o":
x = re.findall("he..o", txt)
print(x)
```

Output:
```
['hello']
```

## 4. `^` - Caret :
The caret symbol ^ is used to check if a string starts with a certain character.

*Example* :
```python
import re

txt = "hello planet"

#Check if the string starts with 'hello':
x = re.findall("^hello", txt)
if x:
  print("Yes, the string starts with 'hello'")
else:
  print("No match")
```

Output:
```
Yes, the string starts with 'hello'
```

## 5. `$` - Dollar :
The dollar symbol $ is used to check if a string ends with a certain character.

*Example* :
```python
import re

txt = "hello planet"

#Check if the string ends with 'planet':
x = re.findall("planet$", txt)
if x:
  print("Yes, the string ends with 'planet'")
else:
  print("No match")
```

Output:
```
Yes, the string ends with 'planet'
```

## 6. `*` - Star :
The star symbol * matches zero or more occurrences of the pattern left to it.

*Example 01* :
```python
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by 0 or more  (any) characters, and an "o":
x = re.findall("he.*o", txt)
print(x)
```

Output:
```
['hello']
```
=========================================================
*Example 02* :
```python
import re
#text = "maan"  # ans = ['maan']
#text = "mn"  # ans = ['mn']
#text = "main"  # ans = []
text = "woman" # ans = ['man']
x = re.findall("ma*n",text)
print(x)
```

Output:
```
['man']
```

## 7. `+` - Plus:
The plus symbol + matches one or more occurrences of the pattern left to it.

*Example 01* :
```python
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by 1 or more  (any) characters, and an "o":
x = re.findall("he.+o", txt)
print(x)
```

Output:
```
['hello']
```
=========================================================
*Example 02* :
```python
import re
#text = "maan" #ans = ['maan']
#text = "mn" #ans = [ ]
#text = "main" #ans = [ ]
text = "woman" #ans = ['man']
x = re.findall("ma+n", text)
print(x)
```

Output:
```
['man']
```

## 8. `?` - Question Mark :
The question mark symbol ? matches zero or one occurrence of the pattern left to it.

*Example 01* :
```python
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by 0 or 1  (any) character, and an "o":
x = re.findall("he.?o", txt) #? refere to numbers i.e. 1to9
print(x)
```

Output:
```
[ ]

In the given example, we got no match, because there were not zero, not one, but two characters between "he" and the "o"
```

=========================================================
*Example 02* :
```python
import re

# txt = "man"   #ans = ['man']
# txt = "mn"    #ans = ['mn']
# txt = "maan"    #ans = []
# txt = "main"    #ans = []
txt = "woman" #ans = ['man']
x = re.findall("ma?n", txt)
print(x)
```

Output:
```
['man']
```

## 9. `{}` - Braces :
Exactly the specified number of occurrences\
Consider this code: {n,m}. This means at least n, and at most m repetitions of the pattern left to it.

*Example 01* :
```python
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed excactly 2 (any) characters, and an "o":
x = re.findall("he.{2}o", txt)
print(x)
```

Output:
```
['hello']
```
=========================================================
*Example 02* :
```python
import re

#txt = "abc dat"    #ans = [ ]
#txt = "abc daat"   #ans = ['aa']
#txt = "aabc daaat" #ans = ['aa', 'aaa']
txt = "aabc daaaat"

x = re.findall("a{2,3}", txt)
print(x)
```

Output:
```
['aa', 'aaa']

* string that has 2 or 3 'a' return using braces.
```
=========================================================
*Example 03* :
* This RegEx [0-9]{2, 4} matches at least 2 digits but not more than 4 digits.
```python
import re

#txt = "ab123csde" #ans = ['123']
# txt = "1 and 2"   #ans = []
txt = "12 and 345673"
x = re.findall("[0-9]{2,4}", txt)
print(x)
```

Output:
```
['12', '3456', '73']
```

## 10. `|` - Alternation :
Vertical bar | is used for alternation (or operator).

*Example 01* :
```python
import re

txt = "The rain in Spain falls mainly in the plain!"

#Check if the string contains either "falls" or "stays":
x = re.findall("falls|stays", txt)
print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
['falls']
Yes, there is at least one match!
```

=========================================================
*Example 02* :
```python
import re

# txt = "cde"  #ans = [ ]
# txt = "ade"  #ans = ['a']
txt = "acdbea"

#Check if the string contains either "a" or "b":
x = re.findall("a|b", txt)
print(x)
```

Output:
```
['a', 'b', 'a']
```

## 11. ( ) - Group:
Parentheses () is used to group sub-patterns. 

*Example 01* :
```python
import re

#txt = "ab xz" #ans = [ ]
#txt = "abxz" #ans = ['b']
txt = "axz cabxz" #ans = ['a', 'b']

x = re.findall("(a|b|c)xz", txt)
print(x)
```

Output:
```
['a', 'b']

* (a|b|c)xz match - any string that matches either a or b or c followed by xz
```
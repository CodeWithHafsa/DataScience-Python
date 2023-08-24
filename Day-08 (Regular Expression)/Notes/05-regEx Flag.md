# Introduction to the Python regex flags:
The regular expression functions like findall, finditer, search, match, split, sub, … have the parameter (flags) that accepts one or more regex flags.

|   Flag         | Alias    |   Description                           |             
|----------------|----------------|---------------------------------------------------|
|re.ASCII| re.A	|	The re.ASCII is relevant to the byte patterns only. It makes the \w, \W,\b, \B, \d, \D, and \S perform ASCII-only matching instead of full Unicode matching.           |
|re.DEBUG| N/A	|	The re.DEBUG shows the debug information of compiled pattern          |
|re.IGNORECASE| re.I	|	perform case-insensitive matching. It means that the [A-Z] will also match lowercase letters.      |
|re.LOCALE| re.L	|	The re.LOCALE is relevant only to the byte pattern. It makes the \w, \W, \b, \B and case-sensitive matching dependent on the current locale. The re.LOCALE is not compatible with the re.ASCII flag.      |
|re.MUTILINE| re.M	|	The re.MULTILINE makes the ^ matches at the beginning of a string and at the beginning of each line and $ matches at the end of a string and at the end of each line.      |
|re.DOTALL| re.S |	By default, the dot (.) matches any characters except a newline. The re.DOTALL makes the dot (.) matches all characters including a newline.      |
|re.VERBOSE| re.X |	The re.VERBOSE flag allows you to organize a pattern into logical sections visually and add comments.      |

* To combine two or more flags, you use the | operator like this:
```
re. A | re.M | re.S
```

## 1. The re.IGNORECASE flag:
The following example uses the findall() function to match all lowercase characters in the set [a-z] in a string:

*Example 01* :
```python
import re
s = 'Python is awesome'
pattern = '[a-z]+' 

#l = re.findall(pattern, s) 
# P is not included in the result because it is not in the set [a-z].
#Output: ['ython', 'is', 'awesome']

l = re.findall(pattern, s, re.IGNORECASE) #include all letters from a-z
#Output: ['Python', 'is', 'awesome']
print(l)
```

Output:
```
['Python', 'is', 'awesome']
```
========================================================
*Example 02* :
```python
import re

str = "KELLy is a Python developer at a PYnative. kelly loves ML and AI"

# with re.I or re.IGNORECASE
# result = re.findall(r"kelly", target_str, re.I)

x = re.findall(r"kelly", str, re.IGNORECASE)
print(x)
```

Output:
```
['KELLy', 'kelly']
```

## 2. The re.MULTILINE flag:
The following example uses the ^ anchor to match one or more word characters at the beginning of a string:

*Example 01* :
```python
import re
s = '''Regex 
Flags'''
pattern ='^\w+'

#l = re.findall(pattern,s) 
# The s string has two lines. The ^ only match at the beginning of the string.
#Output: ['Regex']

l = re.findall(pattern, s, re.MULTILINE) #The s string has two lines. The ^ only match both lines beginning of the string.
#Output: ['Regex', 'Flags']
print(l)
```

Output:
```
['Regex', 'Flags']
```
========================================================
*PRACTICE QUESTIONS* :
* Find 2-digit at the end of each newline. With or without ( re.M or re.MULTILINE flag). 
```python
import re
target_str = "Joy lucky number is 75\nTom lucky number is 25"

#x = re.findall(r"\d{2}$", target_str) 
# without re.M  
#output:['25']

x = re.findall(r"\d{2}$", target_str, re.M) #with re.M  
#output:['75', '25']
print(x) 
```

Output:
```
['75', '25']
```

* Find 3-letter word at the start of each newline. With or Without ( re.M or re.MULTILINE ).
```python
import re
target_str = "Joy lucky number is 75\nTom lucky number is 25"

#x = re.findall(r"^\w{3}", target_str) 
#without re.M
#output: ['Joy']

x = re.findall(r"^\w{3}", target_str, re.MULTILINE) #with re.M
print(x)
```

Output:
```
['Joy', 'Tom']
```

## 3. The re.DOTALL flag :
The dot .+ pattern match one or more characters except for the new line:
*Example* :
```python
import re
s = '''Regex
Flags'''
pattern = '.+'

#l = re.findall(pattern, s) 
#with re.DOTALL
#Output: ['Regex', 'Flags']

l = re.findall(pattern, s, re.DOTALL) #with re.DOTALL
#Output: ['Regex\nFlags']

print(l)
```

Output:
```
['Regex\nFlags']
```

## 4. The re.VERBOSE flag:
the re.VERBOSE flag allows us to add spaces and comments to the regular expression to explain each individual rule.\
The following example shows how to use the re.VERBOSE flag to write a pattern in sections with comments:
```python
import re
s = 'Python 3'

pattern = r'''^(\w+) # match one or more characters at the beginning of the string
               \s*   # match zero or more spaces
              (\d+)$ # match one or more digits at the end of the string'''

l = re.findall(pattern, s, re.VERBOSE)
print(l)
```

Output:
```
[('Python', '3')]
```

## 5. The re.ASCII flag:
re.ASCII flag, the matches will contain only ASCII characters.
```python
import re
s = '作法 is Pythonic in Japanese'
pattern = r'\b\w{2}\b'

#l = re.findall(pattern, s) #withoutre.ASCII
# Output:['作法', 'is', 'in']

l = re.findall(pattern, s, re.ASCII)
print(l)
```

Output:
```
['is', 'in']

`the word 作法 was excluded from the resulting list.`
```
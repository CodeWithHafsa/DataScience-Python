# Regular Expression:
A RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.\
RegEx can be used to check if a string contains the specified search pattern.

### How it works:
```
We love our country! Pakistaz Zinda bad!
ff ffffffffffffffffffttttttttff 
* If we search 'Pakistan'
* If the whole word is present - then it return true otherwise it returns false.
```

### To find methods and attributes of re:
```python
import re
# print(dir(re))
[i for i in dir(re) if "_" not in i]
```

Output:
```
['A',
 'ASCII',
 'DEBUG',
 'DOTALL',
 'I',
 'IGNORECASE',
 'L',
 'LOCALE',
 'M',
 'MULTILINE',
 'Match',
 'NOFLAG',
 'Pattern',
 'RegexFlag',
 'S',
 'Scanner',
 'T',
 'TEMPLATE',
 'U',
 'UNICODE',
 'VERBOSE',
 'X',
 'compile',
 'copyreg',
 'enum',
...
 'search',
 'split',
 'sub',
 'subn',
 'template']
```

## We have some special character for special purpose:
```
. any thing except \n
* zero or many
+ one or may
^ start
$ ending ling
```

# RegEx Functions:
The re module offers a set of functions that allows us to search a string for a match:

|   Function             |Description                           |             
|----------------|-------------------------------|
|`findall`| Returns a list containing all matches           |
|`search`| Returns a Match object if there is a match anywhere in the string           |
|`split`| Returns a list where the string has been split at each match           |
|`sub`| Replaces one or many matches with a string          |

# MetaCharacters :
Metacharacters are characters that are interpreted in a special way by a RegEx engine.
These can be use as 'pattren'
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
## Word boundary concept:
* \b \b
* If you want to apply boundayr concept you have to use "r" befor pattern

# Using r prefix before RegEx
When r or R prefix is used before a regular expression, it means raw string. For example, '\n' is a new line whereas r'\n' means two characters: a backslash \ followed by n.

Backlash \ is used to escape various characters including all metacharacters. However, using r prefix makes \ treat as a normal character.

```python
import re
string = '\n and \r are escape sequences.'
result = re.findall(r'[\n\r]', string) 
print(result)

# Output: ['\n', '\r']
```
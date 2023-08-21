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

## Word boundary concept:
* \b \b
* If you want to apply boundayr concept you have to use "r" befor pattern

## We have some special character for special purpose:
```
. any thing except \n
* zero or many
+ one or may
^ start
$ ending ling
```
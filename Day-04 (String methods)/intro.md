# String Methods
All methods/function, attributes/properties/fields of string - can be determined using 'dir' function.

```python
a = "Python Language!"
print(type(a))
print(dir(a))   #dir return all methods and attributes
```

Output:
```markup
<class 'str'>
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'removeprefix', 'removesuffix', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
```

## Difference Between Methods and Attributes:
A variable stored in an instance or class is called an attribute. A function stored in an instance or class is called a method.

* Action performed by object - is known as 'method'
* It has no action - It only stores value for sometime - 'attribute' or 'property'
* How we can call method or attributes:
    * object_name.method_name()
    * object_name.attribute_name
* With method name we write round bracket. e.g. method_name()

## Help methods:
* help(function)
* help(object_name.method)
* function?
* function??
* ? function
* ?? function
* function(shift press_tab_button)

*Example*
```
* help(print) #help for print function
* print??
* ??print 
```

## Key Points
* String is an object.
* Python data types - belongs to class. Class divides into methods and attributes.
* Jupyter notebook - returns last line
* encoding: e.g. alt+65 = A, alt+97 = a
* UTF-8 are standards for encoding / regular expressions.

## Key Points for Regular Expression
* '.' --- dot means it returns all characters in string individually
* '.+' --- returns complete word of a string, alongwith repeated string.
* '*' ---- returns complete word of a string, but doesnot return repeated string.
* '?' --- means optional in a string. (e.g. if dash include or not it return string.)
* () --- bracket ke andar jo cheez likhtey han, jo return chahiye hoti hai. 
```python
E.g. d = re.findall("(\d{2}:\d{2}:\d{2}) From (.*?) To Everyone : (PIAIC-?\d{5,6})", data)
```

# Concatination and Text Formation
Concatination is used to join text. Concatenating means obtaining a new string that contains both of the original strings.

**Example**

```python
"1" + "1" #string concatination
1 + 1     #integar addition
```

Output:
```markup
'11'
2
```

We can perform string concatenation using following ways:

* Using + operator
* Using format() function
* Using f-string (Literal String Interpolation)
* Using % operator
* Using join() method

## 1. Using + operator:

*Example #1*

```python
a = input("Enter no1: ") #string concatination
b = input("Enter no2: ")
print(type(a), type(b))
print(a+b)
```

Output:
```markup
Enter no1: 7
Enter no2: 8
<class 'str'> <class 'str'>
78
```

*Example #2*
```python
a = int(input("Enter no1:")) #typecasting
b = int(input("Enter no2:"))
print(type(a), type(b))
print(a+b)
```
Output:
```markup
Enter no1: 7
Enter no2: 8
<class 'int'> <class 'int'>
15
```

## New line using '\n':

*Example*

```python
roll_no = 200
name = "Muhammad Qasim"
fname = "Muhammad Aslam"
contact_no = "03152968211"
card = "NED University\nStudent roll no: " + str(roll_no) + "\nStudent name: " + name + "\nFather's name: " + fname + "\nContact no: " + contact_no
print(card)
```

Output:
```markup
NED University
Student roll no: 200
Student name: Muhammad Qasim
Father's name: Muhammad Aslam
Contact no: 03152968211
```

## Space using tab '\t':

*Example*

```python
card = """NED University
Student roll no: \t\t 200
Student Name = \t\t\t Muhammad Qasim
Father's Name = \t\t Muhammad Aslam
Contact no = \t\t\t 03152968211"""
print(card)
```

Output:
```markup
NED University
Student roll no:                 200
Student Name =                   Muhammad Qasim
Father's Name =                  Muhammad Aslam
Contact no =                     03152968211
```

## 2. Using format() function

*Example #1*

```python
roll_no = 200
name = "Muhammad Qasim"
fname = "Muhammad Aslam"
contact_no = "03152968211"
card = """NED University
Student roll no: {}
Student Name: {}
Father's Name: {}
Contact no: {} """ .format(roll_no, name, fname, contact_no)
print(card)
```

Output:
```markup
NED University
Student roll no: 200
Student Name: Muhammad Qasim
Father's Name: Muhammad Aslam
Contact no: 03152968211
```

*Example #2*

```python
roll_no = 200
name = "Muhammad Qasim"
fname = "Muhammad Aslam"
contact_no = "03152968211"
card = """NED University
Student roll no: {2}
Student Name: {0}
Father's Name: {3}
Contact no: {1} """ .format(name, contact_no, roll_no, fname)
print(card)
```
How it works:
```
Index name, contact_no, roll_no, fname
        0      1           2       3
```

Output:
```markup
NED University
Student roll no: 200
Student Name: Muhammad Qasim
Father's Name: Muhammad Aslam
Contact no: 03152968211
```

## 3. Using f-string

*Example #1*
```python
roll_no = 200
name = "Muhammad Qasim"
fname = "Muhammad Aslam"
contact_no = "03152968211"
card = f"""NED University
Student roll no: {roll_no}
Student Name: {name}
Father's Name: {fname}
Contact no: {contact_no} """
print(card)
```

Output:
```markup
NED University
Student roll no: 200
Student Name: Muhammad Qasim
Father's Name: Muhammad Aslam
Contact no: 03152968211
```

*Example #2*

```python
roll_no = input("Enter roll no: ")
name = input("Name: ")
fname = input("Father's Name")
contact_no = input("contact no: ")
print('=====================')

card = f"""NED University
Student roll no:{roll_no}
Student Name: {name}
Father's Name: {fname}
Contact no: {contact_no}"""
print(card)
```

Output:
```markup
Enter roll no:  200
Name:  Muhammad Qasim
Father's Name:  Muhammad Aslam
contact no:  03152968211
=====================
NED University
Student roll no:200
Student Name: Muhammad Qasim
Father's Name: Muhammad Aslam
Contact no: 03152968211
```

*Example #3*
```python
a = f"""(2+2={2+2})"""
print(a)
```

Output:
```markup
(2+2=4)
```
## 4. Using % operator
%s - for string

%d - for number

*Example*

```python
roll_no = 111
name = "Muhammad qasim"
"Student name %s \n roll no: %d" % (name,roll_no)
```

Output:
```markup
'Student name Muhammad qasim \n roll no: 111'
```


# Typecasting
Typecasting - is the method to convert the Python variable datatype into another data type.
* int()
* str()
* float()
* list()
* tuple()
* dict()
* set()

*Example #1*

```python
a = "7"   #string
a = int(a) #int converts string into integar
print("value of a is: ", a, type(a))
```

Output:
```markup
value of a is:  7 <class 'int'>
```

*Example #2*

```python
a = "7"   #string
a = float(a) #int converts string into float
print("value of a is: ", a, type(a))
```

Output:
```markup
value of a is:  7.0 <class 'float'>
```
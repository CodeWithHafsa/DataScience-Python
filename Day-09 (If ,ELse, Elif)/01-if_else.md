## Symbolic AI
* what you can think and write in computer programming language is call Symbolic
* Boolean = 0=False, 1=True
* and, or, not
* reserve key words
    * if
    * else
    * elif

```python
if LOGIC:
    TRUE_body
else:
    FALSE_Body
```
```
Note: LOGIC = TRUE | False
```
# Python Conditions:
Python supports the usual logical conditions from mathematics:

### Comparision Operators:
* Equals: `a == b`
* Not Equals: `a != b`
* Less than: `a < b`
* Less than or equal to: `a <= b`
* Greater than: `a > b`
* Greater than or equal to: `a >= b`

### Logical Operators:
* Returns True if both statements are true: `and`
* Returns True if one of the statements is true: `or`
* Reverse the result, returns False if the result: `not`

These conditions can be used in several ways, most commonly in "if, else, elif statements" and loops.

## If Else:
*Example 01* :
```python
a = 33
b = 200
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

Output:
```
b is greater than a
```
=========================================================
*Example 02* :
```python
if True:
    print("Pakistan")
else:
    print("India")
```

Output:
```
Pakistan
```
=========================================================
*Example 03* :
```python
if False:
    print("Pakistan")
else:
    print("India")
```

Output:
```
India
```

## Create odd and even number program using if else:

*Concept* :
```python
ui = int(input("Enter any number"))
logic = ui%2
logic
```

* If input = 55 #Output = 1 (means number is odd)
* If input = 40 #Output = 0 (means number is even)
* Logic for even number: ui%2 == 0
* Logic for odd number: ui%2 == 1

*Program for even and odd number using if else* :
```python
ui = int(input("Enter any number"))  #if input = 600

if ui % 2 == 0:
    print(f"{ui} This is Even")
else:
    print(f"{ui} This number is Odd!")
```

Output:
```
600 This is Even 
```
========================================================
*Concept of indentation in if else* :
```python
ui = int(input("Enter any number"))

if ui % 2 == 0:
    print(f"{ui} This is Even")
    print("aaa")
    print("aaa")
else:
    print(f"{ui} this number is Odd!")

print("i'm not part of above block")
```

Output:
```
75 this number is Odd!
i'm not part of above block
```

# Elif Statements:

## Create a program of Grading System using elif:

*Hint* :
```
per >= 80 "A+"
per >= 70 "A"
per >= 60 "B"
per >=50 "C"
per >=40 "D"
per >=33 "E"
per <33 "Fail"
```

*Logic* :
```
if logic1:
    statment1
elif logic2:
    statment2
elif logic3:
    statment3
else:
    last_statment
```

*Program of Grading System using elif*:
```python
per = 70

if per>=80:
    print("A+")
elif per >= 70:
    print("A")
elif per>= 60:
    print("B")
elif per>=50:
    print("C")
elif per>40:
    print("D")
elif per>=33:
    print("E")
else:
    print("Fail")
```

Output:
```
A
```
========================================================
*Program of Grading System using elif and 'and' statement*:
```python
per = 99

if per>=0 and per<33: #step1
    print("Fail")
elif per >= 33 and per<40: #step2
    print("E")
elif per>= 40 and per <50:#step3
    print("D")
elif per>=50 and per<60:#step4
    print("C")
elif per>60 and per<70:
    print("B")
elif per>=70 and per<80:
    print("A")
else:
    print("A+")
```

Output:
```
A+
```

# Comprehensive Style / Short Hand for if Else Statement:
```
if Logic:
    true_block
else:
    false_block

# now convert into comprehensive style:
`true_block if Logic else false_block`
```

*Example* :
```python
a = 33
b = 200
"b is greater than a" if b > a else "b is not greater than a"
```

Output:
```
'b is greater than a'
```

## Example of 'and', 'or' and 'not':
*Example of 'and'* :
```python
a = 200
b = 33
c = 500
if a > b and c > a:
  print("Both conditions are True")
```

Output:
```
Both conditions are True
```
========================================================
*Example of 'and'* :
```python
a = 200
b = 33
c = 500
if a > b or a > c:
  print("At least one of the conditions is True")
```

Output:
```
At least one of the conditions is True
```
========================================================
*Example of 'not'* :
```python
a = 33
b = 200
if not a > b:
  print("a is NOT greater than b")
```

Output:
```
a is NOT greater than b
```

# Nested If:
You can have if statements inside if statements, this is called nested if statements.
*Example 01* :
```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

Output:
```
Above ten,
and also above 20!
```
========================================================
*Create a User Login and Password concept using Nested if else*:

#### *Information* :
```
Usecase:
* user input
* password

Logic:
* user_input equal "admin"
* password equal "admin123"
    *Valid user
Message display
```

#### *Solution* :
```python
username = input("Enter user name: \t")

if username == "admin":  # step1 only check username 
    print("Valid user")

    password = input("Enter your password: \t")
    if password == 'admin123': # step2  
        print("Valid user name and password!")
        otp = input("OTP")
        if otp == '123':# step3
            print("Welcome User")
        else:
            print("NotValid OTP blocked now!")
    else:
        print("re enter valid passwordadmin")

else:
    print("Please enter valid user name")
```

Output:
* If input: username = admin and password = admin123 and otp =123
```
Valid user
Valid user name and password!
Welcome User
```
---
* If input: username = abc (so it doenot move further towards password and otp, because username is wrong)
```
Please enter valid user name
```
---
* If input: username = admin and password = 123 (so it doenot move further towards otp, because password is wrong)
```
Valid user
re enter valid passwordadmin
```
---
* If input: username = admin and password = 123 and otp =xyz (so it shows NotValid OTP blocked now!, because otp is wrong)
```
Valid user
Valid user name and password!
NotValid OTP blocked now!
```

### *We can also create User Login Password System using 'and' keyword along with if else loop* :
```python
user = 'admin'
password = 'admin123'
otp = '123'

if user=='admin' and password == 'admin123' and otp == '123':# one layer
    print("Valid user")
else:
    print("Not valid user")
```

Output:
```
Valid user
```

# The pass Statement:
`if` statements cannot be empty, but if you for some reason have an `if` statement with no content, put in the pass statement to avoid getting an error.
```python
a = 33
b = 200

if b > a:
  pass
# having an empty if statement like this, would raise an error without the pass statement
```

Output:
```

#empty set
```
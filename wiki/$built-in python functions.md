# welcome again to the python Tutorial, we gonna see what are the available built-in functions in python!

as we say recently in <a href="https://github.com/NacreousDawn596/Python3-tutorial/blob/main/wiki/data-types.md#welcome-again-to-the-python-tutorial-we-gonna-see-what-are-the-available-types-of-datas-in-python">the data types</a> 
python has some built-in functions like `len()`, `list()`, `str()`, `int()`, `float()`, `upper()`, `lower()`, `clear()`, `range()`, `zip()`, `keys()`, `values()`...

these function only behave with variable, you can't make a program with it because you need interactions with the user, so the first function we gonna learn is the `print()`

# Print()
print() is a function that let you display things to the terminal/console, and it's the most useful function in python because you gonna use for debugging when you gonna master python lol

now let's see how to use it:
```py
my_name = "NacreousDawn596"
print(my_name)
#this will display NacreousDawn596 and a new line in the console 
```
***well, what if we wanna print "https://github.com/" then "NacreousDawn596", what can we do?*** I got you
```py
url = "https://github.com/"
username = "NacreousDawn596"
print(url, end='')
print(username)
#you gonna see in the terminal https://github.com/NacreousDawn596

#but what if we wanna print them, but with another way
print(user, username, sep='')
#you gonna see in the terminal https://github.com/NacreousDawn596
```
ik you're thinking, what if you want to add new lines to the variable?
```py
text = "hello dear,\nI'm NacreousDawn596" #we gonna use what's called backslashes
"""
┌─────────┬─────────────────────────────────────────┐
│ Options │                 Usages                  │
├─────────┼─────────────────────────────────────────┤
│   \n    │               'new line'                │
│   \r    │ 'erase the current line and write text' │
│   \t    │    'for an indentation of 4 spaces'     │
└─────────┴─────────────────────────────────────────┘
"""
```
well, that's the basics the print function, now we saw how to display datas to user, what about taking some datas from the user? we gonna learn that soon

# Input()
input() just like the print() function, it's built-in, but instead of diplaying the datas it takes the datas from the user
, let's see an example
```py
name = input("what's your name?\n=>")
print("hello ", name, "!", sep='')
```
let's how you gonna write this code later after learning python lol:
```py
class person()
  def __init__(self, name, age, height):
    self.name = name
    self.age = age
    self.height = height
name = input("what's your name?\n=>")
age = input("what's your age?\n=>")
height = input("what's your height?\n=>")
user = person(name, age, height)
print("hello", user.name, ", how was your", user.age, "years of living?\nbtw, how did you get to", user.height, "? XD")
```
lmao, but first, let's learn step by step, you can learn more things from the <a href="https://github.com/NacreousDawn596/Python3-tutorial">main page</a> ^^

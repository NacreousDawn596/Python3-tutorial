# welcome again to the python Tutorial, we've saw the basics now in the previous times, now let's learn **coding** step by step to make our first program
our program will be a cashier in a book store.
 let's begin begin by adding items (books) and prices in the shop
 
```py
items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
```
now let's make a client come and buy something
```py
items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
client_balance = 200
client_bag = {}
print("\n".join(list(items.keys())))
item = input("write what item you wanna buy\n=>")
client_balance -= items[item]
client_bag.append(item)
print("nice, now you got ", ", ".join(client_bag), "\nyour current balance is: ", client_balance, sep='')
```
okay, but what if the client wanna buy a loooot of things, how to do it?

well, to do that, we have to learn about loops

# While Loops
while loops are just some loops that repeat the code inside, let's see an example:
```py
n = 0
while n <= 10:
  n += 1
  print(n)
#this will write all numbers from 1 to 10
```
the while loops are just too easy ;-;
, now let's add them to our code:
```py
items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
client_balance = 200
client_bag = []
while True!
  print("\n".join(list(items.keys())))
  item = input("write what item you wanna buy\n=>")
  client_balance -= items[item]
  client_bag.append(item)
print("nice, now you got ", ", ".join(client_bag), "\nyour current balance is: ", client_balance, sep='')
```
wait, wait, wait, but what if the client wanna stop buying, what should we do?? I got you. so we gonna learn about something called conditions

# Conditions
conditions are just some simple lines of code to check the condition between values
```
┌─────────┬──────────────────────────────────────────────────────────────────┐
│-operator│                              Values                              │
├─────────┼──────────────────────────────────────────────────────────────────┤
│ a == b  │  returns True if they are equal otherwise it gonna return False  │
│ a != b  │                  returns True if they are equal                  │
│ a <= b  │            return True if a is smaller or equal to b             │
│ a >= b  │             return True if a is bigger or equal to b             │
│  a < b  │            return True if a is strictly smaller to b             │
│  a > b  │             return True if a is strictly bigger to b             │
└─────────┴──────────────────────────────────────────────────────────────────┘

┌────────────────────┬───────────────────────────────────────────────────────┐
│     operators      │                        Values                         │
├────────────────────┼───────────────────────────────────────────────────────┤
│ a != b and a <= b  │    ' returns True if both conditions are verified'    │
│ a == b or a >= b   │ ' returns True if one of the conditions are verified' │
│    not a == b      │    " returns True if the condition isn't verified"    │
└────────────────────┴───────────────────────────────────────────────────────┘

```
let's see an example:
```py
my_name = "NacreousDawn596"
if my_name == "NacreousDawn596":
  print("that's true!")
```
the output of this code will be `that's true!`
but what if we want to check multiple conditions?? you just have to replace if by elif lol, see the example below
```py
my_name = "NacreousDawn596"
if my_name == "Nac":
  print("Hello Nac")
  
elif my_name == "NacreousDawn596":
  print("hello NacreousDawn596")
```
the output of this code will be `hello NacreousDawn596`

now we gonna see if the all conditions aren't verified,
```py
my_name = "NacreousDawn"
if my_name == "Nac":
  print("Hello Nac")
  
elif my_name == "NacreousDawn596":
  print("hello NacreousDawn596")
  
elif my_name == "useless garbage":
  print("hello useless garbage")

else:
  print("who tf are you?")
```
the output of this code gonna be `who tf are you?`

now, let's see a more complexe example

```py
x = 9
y = 10

if x == y:
  print("yay! condition 1")
elif x != y:
  print("yay! condition 2")
elif x <= y:
  print("yay! condition 3")
elif x >= y:
  print("yay! condition 4")
elif x < y:
  print("yay! condition 5")
elif x > y:
  print("yay! condition 6")
```
the output will be:
```
yay! condition 2
```
now we understood what conditions are, let's upgrade out code:
```py
items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
client_balance = 200
client_bag = []
while True:
  print("\n".join(list(items.keys())))
  item = input("write what item you wanna buy (write EOF when you finish)\n=>")
  if item.lower() == "eof":
    break #to break the while loop
  client_balance -= items[item]
  client_bag.append(item)
print("nice, now you got ", ", ".join(client_bag), "\nyour current balance is: ", client_balance, sep='')
```
well, the code seems cursed a bit, let's make it easier by adding for loops!
# For Loops
For loops are just loops that uses lists, the length of that list = the time repeats, let's see an example:
```py
for i in range(0, 5): #if you didn't understand range() go and read previous docs
  print(i)
```
this will print:
```
0
1
2
3
4
```
now, let's use it with another list:
```py
my_usual_list = ["NacreousDawn596", 16, 172.3]
for i in my_usual_list: #you can replace i by whatever you want, it's just a variable
  print(i)
```
the output will be:
```
NacreousDawn596
16
172.3
```
**Conclusion:** there are no for loops in python, they are all ForEach loops

now, let's add it to our code:
```py
items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
client_balance = 200
client_bag = []
while True:
  #print("\n".join(list(items.keys())))
  for book in items:
    print(book, ": ", items[book], sep='') 
  item = input("write what item you wanna buy (write EOF when you finish)\n=>")
  if item.lower() == "eof":
    break #to break the while loop
  client_balance -= items[list(items)[item]]
  client_bag.append(list(items)[item])
print("nice, now you got ", ", ".join(client_bag), "\nyour current balance is: ", client_balance, sep='')
```
***but it's too long to write the whole name, what should I do?***, look at this trick:
```py
items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
client_balance = 200
client_bag = []
while True:
  #print("\n".join(list(items.keys())))
  for book in range(len(items)):
    print(book, ": ", list(items.keys())[book], "=> price: ", items[list(items.keys())[book]], sep='') 
  item = input("write the index of the item you wanna buy (write EOF when you finish)\n=>")
  item = int(item)
  if item.lower() == "eof":
    break #to break the while loop
  client_balance -= items[list(items)[item]]
  client_bag.append(list(items)[item])
print("nice, now you got ", ", ".join(client_bag), "\nyour current balance is: ", client_balance, sep='')
```
**btw**, we can also use for loops in lists, like this:
```py
urls = ["https://github.com/", "https://instagram.com/", "https://www.google.com/search?q="]
my_urls = [url + "NacreousDawn596" for url in urls]
print(my_urls)
```
the output displayed is:
```
['https://github.com/NacreousDawn596', 'https://instagram.com/NacreousDawn596', 'https://www.google.com/search?q=NacreousDawn596']
```

***okay, okay, but what if we wanna make the code more efficient?*** well, to do that, we gonna learn functions

# Functions
functions. yeah, function. they are named function, but who tf chose the keyword `def` to declare them?????

let's see a quick demonstration: functions not like variables (in other languages like javascript they can be used as variables), they are used to minimize the code and optimize it, like instead of writing the same thing multiple times, you can save time by using functions, let's see an example, it's an old example that we used <a href="https://github.com/NacreousDawn596/Python3-tutorial/edit/main/wiki/basics.md#conditions">here, the third one</a>, let's use it again
```py
def say_my_name(name): #yeah, we declare them using the keyword def
  print("hello", name)

my_name = "NacreousDawn596"
if my_name == "Nac":
  say_my_name(my_name)
  
elif my_name == "NacreousDawn596":
  say_my_name(my_name)
  
elif my_name == "useless garbage":
  say_my_name(my_name)

else:
  print("who tf are you?")
```

as you see here, same writing, but different output each time I change my the variable my_name


**btw**, we can't edit a variable outside the function, like so:
```py
x = 10
def my_func():
  x = 9
print(x)
my_func()
print(x)
```
the output will be the same, nothing gonna change.

***okay, but what if we wanna edit a  variable  with a function, what can we do?***

you can use these tricks:
```py
###########first way
x = 10
def my_func():
  global x
  x = 9
print(x)
my_func()
print(x)
```
as you see here, the variable x changed due to the function `my_func()` using the keyword `global`
the output is:
```
10
9
```
let's see another way
```py
###########first way
x = 10
def my_func():
  return 5
print(x)
x = my_func()
print(x)
```
***woah, here the variable x changed too!*** yeah, thanks to `return` that return a value from a function

now let's add functions to out code!
```py
def buy(item):
  global client_balance, client_bag
  client_balance -= items[item]
  client_bag.append(item)

items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
client_balance = 200
client_bag = []

while True:
  #print("\n".join(list(items.keys())))
  for book in range(len(items)):
    print(book, ": ", list(items.keys())[book], "=> price: ", items[list(items.keys())[book]], sep='') 
  item = input("write the index of the item you wanna buy (write EOF when you finish)\n=>")
  item = int(item)
  if item.lower() == "eof":
    break #to break the while loop
  buy(list(items)[item])
  
print("nice, now you got ", ", ".join(client_bag), "\nyour current balance is: ", client_balance, sep='')
```
***WTF are you talking about??????? an error is always raising "AttributeError: 'int' object has no attribute 'lower'", are you conscious of what are you doing???***

yeah, no worry, to pass that error, we gonna use python's errors handling
# Errors Handling
list of all possible errors:
```
┌───────────────────────┬──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│         Errors        │                                                   when is raises?                                                            │
├───────────────────────┼──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│    AssertionError     │                                           'Raised when an assert statement fails.'                                           │
│    AttributeError     │                                    'Raised when attribute assignment or reference fails.'                                    │
│       EOFError        │                                                   'Raised when the input'                                                    │
│  FloatingPointError   │                                       'Raised when a floating point operation fails.'                                        │
│     GeneratorExit     │                                               "Raise when a generator's close"                                               │
│      ImportError      │                                       'Raised when the imported module is not found.'                                        │
│      IndexError       │                                    'Raised when the index of a sequence is out of range.'                                    │
│       KeyError        │                                      'Raised when a key is not found in a dictionary.'                                       │
│   KeyboardInterrupt   │                                        'Raised when the user hits the interrupt key '                                        │
│      MemoryError      │                                        'Raised when an operation runs out of memory.'                                        │
│       NameError       │                               'Raised when a variable is not found in local or global scope.'                                │
│  NotImplementedError  │                                                'Raised by abstract methods.'                                                 │
│        OSError        │                                 'Raised when system operation causes system related error.'                                  │
│     OverflowError     │                     'Raised when the result of an arithmetic operation is too large to be represented.'                      │
│    ReferenceError     │                     'Raised when a weak reference proxy is used to access a garbage collected referent.'                     │
│     RuntimeError      │                                'Raised when an error does not fall under any other category.'                                │
│     StopIteration     │                                                       'Raised by next'                                                       │
│      SyntaxError      │                                     'Raised by parser when syntax error is encountered.'                                     │
│   IndentationError    │                                        'Raised when there is incorrect indentation.'                                         │
│       TabError        │                             'Raised when indentation consists of inconsistent tabs and spaces.'                              │
│      SystemError      │                                      'Raised when interpreter detects internal error.'                                       │
│      SystemExit       │                                                     'Raised by sys.exit'                                                     │
│       TypeError       │                       'Raised when a function or operation is applied to an object of incorrect type.'                       │
│   UnboundLocalError   │ 'Raised when a reference is made to a local variable in a function or method, but no value has been bound to that variable.' │
│     UnicodeError      │                              'Raised when a Unicode-related encoding or decoding error occurs.'                              │
│  UnicodeEncodeError   │                                'Raised when a Unicode-related error occurs during encoding.'                                 │
│  UnicodeDecodeError   │                                'Raised when a Unicode-related error occurs during decoding.'                                 │
│ UnicodeTranslateError │                               'Raised when a Unicode-related error occurs during translating.'                               │
│      ValueError       │                        'Raised when a function gets an argument of correct type but improper value.'                         │
│   ZeroDivisionError   │                          'Raised when the second operand of division or modulo operation is zero.'                           │
└───────────────────────┴──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```
in python, you can catch errors like so:
```py
try:
  name = "Nac"
  print(int(nac))
except Exception as err: #this is avoiding all types of errors
  print("it cannot be converted to int, here's the error raised:")
  print(err)
```
let's see how to catch an error:
```py
try:
  name = "Nac"
  print(int(name))
except ValueError:
  print("it cannot be converted to int")
```
what about catching two or multiple erros?
```py
try:
  name = "Nac"
  print(int(name))
except (ValueError, MemoryError):
  print("it cannot be converted to int, or your memory is full")
```
now we learned catching errors, let's add them to our code
```py
def buy(item):
  global client_balance, client_bag
  client_balance -= items[item]
  client_bag.append(item)

items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}
client_balance = 200
client_bag = []

while True:

  #print("\n".join(list(items.keys())))
  for book in range(len(items)):
    print(book, ": ", list(items.keys())[book], "=> price: ", items[list(items.keys())[book]], sep='') 
  item = input("write the index of the item you wanna buy (write EOF when you finish)\n=>")
  
  try:
    item = int(item)
    buy(list(items)[item])
  except ValueError:
    try:
      if item.lower() == "eof":
        break #to break the while loop
    except:
      pass
    print("please enter a valid integer")
  
print("nice, now you got ", ", ".join(client_bag), "\nyour current balance is: ", client_balance, sep='')
```
**wait!** I forgot to tell you the use of `pass`, it's simply used to avoid blank blocks when there's nothing to execute, here's an example
```
if True:
  pass
```
nothing gonna be achieved, as if you haven't even ran the code.

***wait, wait, wait, I think we gave a lot important to the code than the client, what if we wanna make it better?*** to do that, let's use classes

# Classes
class are neither functions or variables, yet it can contains both of them and even moore, and it's declared using the keyword `class`
```py
class Client(): #you can change the word Client
  def __init__(self, name, bag, balance):
    self.username = name
    self.bag = bag
    self.wallet = balance
    
  def buy(self, item): #and yes, you can add functions inside classes!! amazing, right?
    self.wallet -= items[item]
    self.bag.append(item)

client = Client("NacreousDawn596", [], 2000)
items = {"star wars": 8, "one piece": 2, "the night of death": 7, "naruto episode 53": 2.6}

while True:

  #print("\n".join(list(items.keys())))
  for book in range(len(items)):
    print(book, ": ", list(items.keys())[book], "=> price: ", items[list(items.keys())[book]], sep='') 
  item = input("write the index of the item you wanna buy (write EOF when you finish)\n=>")
  
  try:
    item = int(item)
    client.buy(list(items)[item])
  except (ValueError, IndexError):
    try:
      if item.lower() == "eof":
        break #to break the while loop
    except:
      pass
    print("please enter a valid number")
  
print("hello ", client.username, "\nnice, now you got ", ", ".join(client.bag), "\nyour current balance is: ", client.wallet, sep='')
```

well, that's all we need to learn in this doc, you can go back to <a href="https://github.com/NacreousDawn596/Python3-tutorial">the main page</a> and learn something new! :D

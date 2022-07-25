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
# Loops
I will continue tomorrow...

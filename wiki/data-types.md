<center>
  <h1>welcome again to the python Tutorial, we gonna see what are the available types of datas in python!</h1>
</center>

in python, like any other coding languages, it has data types, such as string, integers, floats, lists, dicts... but the amazing thing about python is that the datas dynamic are dynamic, unlike java or C.

let's begin with the basic one, **String**
# Strings
strings are a data type of variable that contains alpha numeric text, let's see how we can declare a string:
```py
my_name = "NacreousDawn596" #this is a string
my_name = 'NacreousDawn596' #this is a string too
my_name = """my name is:
          NacreousDawn596""" # and yes, that's a string
my name = '''my name is:
          NacreousDawn596''' # without forgetting this one too lol
```
in python, you have the ability to make the whole string with uppercases or lowercases, let's see an example:
```py
my_name = "NacreousDawn596".upper() #this is an uppercased string
my_name = "NacreousDawn596".lower() #this is an lowercased string
```
and we can also capitalize the string like so:
```py
my_name = "NacreousDawn596".lower().capitalize() #this string was lowercased then capitalized
```
I know you were thinking about how can we concatenate two strings (ofc you weren't think of this, lmao), to do so, you have to:
```py
my_username = "NacreousDawn596"
my_url = "https://github.com/"
full_url = my_url + my_username
```
I think that's enough for string, let's hop on integers!
# Integers
well, a simple explanation of what intergers are: they are thee basic number that a 6yo baby knows (0, 1, 2, 3, 4...), he may not know the negative numbers, but you should!

let's see how we can define them:
```py
my_age = 16
```
as easy as drinking water _(sorry for those who have some illnesses)_

what's the first thing that we think of when we hear the word "number"? if it's not maths then quite living XD. and yeah, in python maths exists, and you can use it  like the example below :D
```py
my_age = 10 + 5 + 1 #for the addition
my_age = 20 - 4 #for substrating
my_age = 32 / 2 #for dividing
my_age = 4 * 4 #for multiplicatings
```
is there something easier than this? if it's not drinking water then I'm sorry.

now that we've finished with integers, let's see what floats are
# Floats
what are floats? floats are the decimal numbers that 9yo children start to learn at school. ***nac, stop joking! tell use how to use them in python!!***, well, if you want to, see the example of how we can define them:
```py
my_height = 172.3 #yeah, this is a float, and my height is 172.3cm btw
```
**wait! note this:**
```py
temperature = 23.0 #this is a float
temperature = 23 #BUT THIS ISN'T A FLOAT, IT'S AN INTEGER!
```
and you can also do maths with floats like so:
```py
x = 1.5 + 3 
x = 4 - 8.2
x = 2.5 * 2
x = 10 / 3
# all of these are floats
```
**btw**, do you still remember at the beginning when I said "but the amazing thing about python is that the datas dynamic are dynamic, unlike java or C."?
let's demonstrate it here:
```py
x = "NacreousDawn596" #this is a string
x = 16 #this is an integer
x = 172.3 #this is a float
```
as you see, you don't have to define the variable type everytime... and that's time-saving, or life-saving!
 
now we saw the basic variable that most of us should know, let's increase the difficulty a bit and see what lists are,

#Lists
quick explaination: lists are like containers that contains datas that we can use later, and each data in it has a place that's called an index, it always starts with 0.
 
now when say a quick demonstartion, let's how to use it:
```py
my_list = ["NacreousDawn596", 16, 172.3] # a list can be defined with brackets that can contain all types of datas
#                0            1     2    # these are the indexes of the datas, as I said "and each data in it has a place that's called an index, it always starts with 0."
```
***okay nac, now that we have the datas stored inside, how can we use them?***, well, it's not as hard as you think,
```py
my_list = ["NacreousDawn596", 16, 172.3]
my_name = my_list[0]
my_age = my_list[1]
my_height = my_list[2]
```
***wait a minute, now that we know the index of the first item of a list is 0, so what's the index of the last one if we are too lazy to count?***, ummm, take a look at this:
```py
my_list = ["NacreousDawn596", 16, 172.3]

#I have two solutions for you:

#first one is to count the length of the list then substract 1 because it begin by 0 and not 1, to do that, try this:
my_list_items = len(my_list) #this is the number of items in the list
my_list_items -= 1 # or my_list_items = my_list_items - 1
last_item = my_list[my_list_items] # and this should be: 172.3

#the second solution is the easiest:
last_item = my_list[-1] # 🥲, this should be 172.3 too
```
***but what is I want to add or edit and item, or even clear the list or other things that make my life easier, can you explain?*** I got you, take a look at this:
```py
my_list = ["NacreousDawn596", 16, 172.3]

#let's say you wanna change something in the list, let's take for example the first item
new_name = "Nac"
my_list[0] = new_name # now the new list is ["Nac", 16, 172.3]
#######################################################################################################################################################
#now we gonna add the city where I'm currently living in:
my_city = "Casablanca"
my_list.append(my_city) #we use append() to add a new item to the list
#now, our list is ["Nac", 16, 172.3, "Casablance"]
#######################################################################################################################################################
#let's see how to clear a list with two ways:

#first way:
my_list.clear()

#second way:
my_list = []
#######################################################################################################################################################
#let's say that you want to convert a string into a list, and each item in that list will contain a character, see the example below:
my_name = "NacreousDawn596
my_list = list(my_name) #the list now is: ['N', 'a', 'c', 'r', 'e', 'o', 'u', 's', 'D', 'a', 'w', 'n', '5', '9', '6']
#######################################################################################################################################################
#but what if you wanna generate a list that contains number from 1 to 10, you won't do [0, 1, 2, 3...] ofc lol, you gonna use the method range()
#so basically the use of range is like so: range(min, limite)
numbers = range(0, 11) #but wait, this isn't a list, what are you talking about??
numbers = list(numbers) #now we are talking :)
#now numbers is equal to [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
well, that's all what a beginner in python should know.
 now we understood the lists, wanna try to understand dicts too?
 
#Dicts
dicts are literally just json in python (with some changes)
**the changes:**
in python, you can do `{"name": "nac"}` while in json you can't, you need to write it like so: `{'name': 'nac'}`... wait, I forgot to tell you about booleons, let's see them quickly to continue,

**booleons:** they are simply just True or False, let's see an example:
```py
1 + 2 == 3 #this return True | we use the operators to verify them, here's a list of all operators:
"""
a == b | returns True if they are equal otherwise it gonna return False
a != b | returns True if they are equal
a <= b | return True if a is smaller or equal to b
a >= b | return True if a is bigger or equal to b
a < b | a <= b | return True if a is strictly smaller to b
a > b | a <= b | return True if a is strictly bigger to b
```
that's it, let's continue explaining dicts, as we were saying, let's see more changes:
in python you can do `{"am I a psycho?": True}` whi le in json you have to do `{'am I a psycho?': true}`...
now let's see how to use dicts:
```py
dictionnary = {"me": "psycho"}
```
that's how we define it, and we can use all types of variables just like lists, see the example below:
```py
dictionnary = {"me": {"age": 16, "name": "nac", "height": 172.3, "hobbies": [{"coding": {"do I like it?": "I love it"}}]}}
```
like in this example, we stored almost all types of variables, now let's see how to use them:
```py
dictionnary = {"me": {"age": 16, "name": "nac", "height": 172.3, "hobbies": [{"coding": {"do I like it?": "I love it"}}]}}
my_infos = dictionnary["me"]
my_age = my_infos["age"]
my_hobby = my_infos["hobbies"]
fr = my_hobby["coding"]
```
let's see now how can we convert a dict into a list
```py
temperatures = {"hot": 45, "ambient": 23, "cold": 10, "what's the limite?": 273.15}
#let's convert it into a list
temperatures_list = zip(list(temperatures.keys()), list(temperatures.value())) 
#we use keys() method to get the list of keys like "hot", "cold"...
#we use values() method to get the list of values like 45, 10...
```
guess what, that's it, you've just learned all the basics of variables

# let's see how to convert them:
I already use it before, but I will write it again
```py
to convert anything into a string you can use the method str(my_variable)
to convert a float or a string that contains only numbers into integer, use the method int(my_variable)
to convert an integer or a string that contains only numbers into float, use the method float(my_variable)

well, <a href="https://github.com/NacreousDawn596/Python3-tutorial">now go to the main page</a> and learn something new ^^

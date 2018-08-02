All assignments for python section will be added here.

### 1. Hello World Script
This is the first program for any language. Create a python script that prints "Hello World" to the command-line.

### 2. Odd or Even Script 
Take the following code and make sure
```python
# copy this code into your file and use it for this assignment.

# this is an example function
def add_ten(x):
     print x + 10  # notice this is indented

# YOUR CODE WILL GO INTO THIS FUNCTION
def print_even_or_odd(x):
   # 1. remember the logic in this function must be indented
   # 2. to determine whether a number is even: x % 2 is EQUAL to 0
   # 3. to determine whether a number is odd: x % 2 is NOT EQUAL to 0
   # basic logic:
   #
   # if x % 2 is equal to 0, then print "even"
   # else then print "odd"
   #
   # code the above logic in this function
   


a = 894754
b = 1
c = 0
d = -1
e = 2
f = 99999999993449

# call the example function, example output should be:
#
# 894764
# 
add_ten(a) # this will send the variable "a" to add_ten() and store contents of "a" into "x" and then do the operation

# now you must call print_even_or_odd() and the output should be what you expect
print_even_or_odd(a)
print_even_or_odd(b)
print_even_or_odd(c)
print_even_or_odd(d)
print_even_or_odd(e)
print_even_or_odd(f)

# this should print "even"!!!!!
```

### 3. String Manipulation
You will write a function that Copy the below code and finish writing the function.
```python
def change_e_to_3(x):
     # your code goes in here, print the output
     
change_e_to_3("Cheetah") # example output for this should be "Ch33tah"
change_e_to_3("Eat before you SLEEP") # example output for this should be "3at b3for3 you SL33P" notice the uppercase handling
change_e_to_3("TRES LECHE is 3 leches") 
```

### 4. Functions that RETURN data
You will write a function that uses the keyword ```return``` to return data from your function to a new variable. For instance, let's assume we have a function called ```does_this_string_say_happy()``` and all it does is return a ```True``` or ```False```. We can write a script that looks like:
```python
def does_this_string_say_happy(string_variable):
    if string_variable == "happy":
       return True
    else:
       return False
       
a = "happy"
b = does_this_string_say_happy(a) # we send our function the variable (a) which contains the STRING data "happy"
print b
```
So functions can take data, manipulate it, then return it back to our main program for more processing.

Your goal is to fill out a function returns the length of a string! For example, the string ```"asdf"``` has a length of 4 (it has 4 characters: "a", "s", "d", "f"). Your function should return the length of ANY string.
```python 
def length_of_string(y)
     # your logic goes here
     
a = "owierunfgldlkg;aoijtlgjklsndf;oitjglksjdflkjsdofijsdf"
b = length_of_string(a)
c = b * 10
print "The length of " + a + " is " + str(b) + " and if you multiply that by 10 then you get " + str(c) 
# you can't print strings and integers in the same line, so we cast our integers stored in (a) and (c) to be strings with
# the function str()
```

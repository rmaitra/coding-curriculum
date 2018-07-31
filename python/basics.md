## Bash Basics
Unix is an operating system that many computer programmers use. Understanding how to use a Unix terminal is important for developers. Bash stands for "Bourne again shell" which is basically an interpreter for Unix. For Windows 10, make sure you install a linux subsystem (follow the link instructions):

https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/

When you get the terminal on Windows up, try out the following commands. In the terminal you will have a prompt and a cursor blinking. There are several commands that you need to know (the prompt is denoted with the dollar sign $):
```
$ ls                        <--- list the contents of the current directory

$ cd SOME_DIRECTORY_NAME    <--- change current directory to directory called "SOME_DIRECTORY_NAME"

$ mkdir NAME                <--- create a directory with name="NAME"

$ cp FILENAME NEW_FILENAME  <--- copy a file and create a new file with same contents

$ less FILENAME             <--- open a file called FILENAME and read the contents to the screen

$ pwd                       <--- print which directory you are in (sometimes you can get lost)

$ rm FILENAME               <--- remove a file named FILENAME

$ ifconfig                  <--- print your systems network configurations (check your ip address, etc)

$ vi FILENAME               <--- vi is a text-editor for the terminal. you can open up a file and edit it, or you can create a new file.
```
Remember that when you enter a command in the terminal you need to hit enter for the terminal to read the command. 

![gif of bash](https://github.com/rmaitra/sonny-learns/blob/master/week1/bash_basics.gif)

**DON'T BE AFRAID OF THE TERMINAL!** People get scared of the terminal, but it's such a wonderful tool and with the right guidance it can be learned easily! 

## Python Basics
What is python? It's a language. A scripting language to be more specific. It is used by scientists, software developers, accountants, all sorts of people to do anything from manipulating CSV files (your basic Excel files), mining swaths of data across multiple SQL databases, generating jaw-dropping data visualizations, to artificially intelligent bot networks. It's also fairly easy to understand. Coders talk about pointers, or memory allocation, etc; terminology that tends to scare first-time coders. Python removes a lot of that scary behind-the-scenes logic and creates an easy place for coders to learn. 

Let's start by creating a simple python program, open up the terminal, open up your favorite text-editor and create a file:

```python
# this is a comment in python, denoted by the hashtag in front of this text
# none of this will be read by the computer when python compiles this file 
# to binary

print "Hello World"    # <--- this is the print command. we are printing a string to STDOUT (standard output, or in this case, the terminal when we run it)
```
Save the program with the extension **.py**. An example could be **hello_world.py**. Then in the terminal, ```$ cd ``` to the directory in which the file is located and run the python file with:
```
$ python hello_world.py
```
The string **Hello World** will be printed to the screen. Easy right? Here is a gif of this:

![gif of python helloword](https://github.com/rmaitra/sonny-learns/blob/master/week1/python_hello_world.gif)

### Variables and Data Types in Python
You learned the **print** command. Well there are many commands built into python. We will get into those. First let's go over data types that you can store information in. These are common to ALL languages:

- **strings**: basically text. Denoted by the double quotes or single quotes. A lot of programming can be string manipulation. Technically they are arrays of characters (a character being "c" or "e").
- **integers**: a whole number like 1 or 5849875.
- **floats**: a decimal number like 3.4 or 94875.495. These numbers are stored in memory differently than integers.
- **booleans**: True or False. That's it. Those two values and only those two.
- **arrays**: a grouping of any of the above data-types in a sequence! An array in python will look something like:

```python 
[1, 2, "I am a string", True, 4.5, ["this is an array in an ARRAY!", 23] ]
```

- **dictionaries** (or objects): an object that holds data that can be accessed through a **key**. This is more complicated to understand but is INCREDIBLY important and useful:

```python
# below is a dictionary, or in most other languages, an object. it contains KEYS and VALUES. 
# the values can be accessed in the dictionary via their key. this is a GREAT way to organize data in code

rajs_bank_data = {         # this is the start of the dictionary, notice it is being stored in a VARIABLE
   "total_money":1849575,  # this is an integer that can be accessed by the KEY "total_money"  
   "account_number":1094859873,
   "bank_name": "Bank of India"
} # this is the end of the dictionary

# the object is being stored in a variable called rajs_bank_data
# the variable rajs_bank_data is a dictionary
print rajs_bank_data["total_money"]
print rajs_bank_data["account_number"]
print rajs_bank_data["bank_name"]
``` 

You can store any of these data-types in a variable. Variables can be named whatever you'd like them to be named:
```python
oshkosh = "this is a string"
another_variable_with_a_name = 2039483
this_is_an_array = [1, 2, 4]
boolean_variable = True
i_am_a_dictionary = { "this_is_the_key":"I am some string data in the value part of the dictionary, access me like i_am_a_dictionary['this_is_the_key']" }
```
Pretty simple. 

### Operators in Python
Now you need to manipulate the data! In order to manipulate the data, you need operators. Operators are like:
```python
2 + 2 # (plus for addition)
3 - 4 # (minus for subtraction)
4 * 5 # (asterisk for multiplication)
blah_variable_name = 345 # (equals to store data in variables!)
3454 == "this is a string" # (2 equal signs to return whether two things are the same value) this should return False
3454 != "this is a string" # (check if 2 pieces of data are NOT equal) this should return True!
```
You can open up the terminal and play with data types and variables in the **python interpretor** like so:
```
$ python 
```
Here is a gif doing this:

![gif of python terminal](https://github.com/rmaitra/sonny-learns/blob/master/week1/python_terminal.gif)

### For Loops, While Loops
Loops are used to iterate through arrays and objects and do actions on specific elements within the arrays or objects. A **for** loop will iterate from the beginning of an dictionary or array until the end of it:

```python
for(i in [1,2,3,4]):
    print i
    
# the output of this program will be:
# 1
# 2
# 3
# 4
```

A **while** loop will iterate until a condition is met:

```python
i = 0
sum = 0
while(i <= 3):
    sum = sum + i
    i = i + 1
    
    print "i: {}".format(i) # this is a way to print a string and int onto the same line using "{}".format(SOME_INT_VARIABLE)
    print "sum: {}".format(sum) # this is a way to print a string and integer onto the same line

# the output of this program will be
# i:1
# sum:1
# i:2
# sum:3
# i:3
# sum:6
```

### Functions in Python
Functions are small snippets of logic that you can easily call over and over again in a single line of code. Here is an example of a function that will print the contents of any array one element at a time:
```python

# "def" is a keyword that is used to define a function
# after "def" we have the name of the function (can be anything)
# then we have the data that we pass to the function in parantheses
# this "(array_variable)" is called the arguments

def this_function_will_print_an_array(array_variable):
    for(i in array_variable):
         print i
         
new_array = [1,2,"hello","four"]
this_function_will_print_an_array(new_array)  # call the function "this_function_will_print_an_array"

# output of this program:
# 1
# 2
# hello
# four
```
The reason we create functions is so that we don't have to write the same code a BUNCH of times. We can just call the snippet of logic whenever we need to do it again. 


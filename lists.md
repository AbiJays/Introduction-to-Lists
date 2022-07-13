# An Introduction to Lists

**10-15 minutes**

Hello there, today we are looking at and understanding Python Lists, our learning objectives for this speedy run-down are... 

### Learning Objectives
 - Understand the general concept of what a list is
 - Be able to create a list
 - Be able to access an element in a list.
 - Be able to alter list items by 
    - Changing them/ reassigning them
    - Adding items
    - Removing items
- Be able to access information regarding our list such as
    - Length of the list


To start with, let's get to grips with what a list actually is:

A list, as I'm sure you are aware in general is a group of elements/ objects, be that your favourite holiday destinations, snacks, or task list for instance.

And a Python list is just that, it is a mutable, ordered data structure, a collection of objects, stored under one variable: i.e. a name.
For instance that Task List could consist of

Task List
- eat pie
- watch clouds
- drink water

and anything else you have planned for the day. This list of elements is stored or contained under the name, or variable of Task List. 

Does that make sense?


## So let's get to making our very first Python list.

We need to create a file in order to do this so in your terminal in your work folder, we are going to type 

```
touch lists.py
```

and hit enter

we are then going to open our new file 'lists' in Virtual Studio Code by typing in terminal

```
code .
```

## Commence listing

We start by giving our list a name and because you cannot use spaces within variables we will follow convention and use an underscore to separate the words. We will type task_list

In lists.py we are going to type our variable name of:

```python
# lists.py

task_list
```
There are other naming conventions but this is not important right now as this is what we are going to use.

To relate our list items to our list name, i.e. variable we use the assignment operator: "="

```python
# lists.py

task_list = 
```

And then we add our items, in Python this requires using square brackets - almost like the edges of our container.

```python
# lists.py

task_list = []
```

## Elements

We will separate the objects in our list with commas, and due to the objects consisting of strings we will need to contain them in quotation marks:

```python
# lists.py

task_list = ["eat pie", "watch clouds", "drink water"]
```
Then we'll save it!

## Now What
So we've created a beautiful list, but now what. Well, to check our list exists under the variable name we need to add a return statement, so the list is actually returned to us. To do this we will use the print function. This is a built in function of Python and prints whatever you specify.

```python
# lists.py

task_list = ["eat pie", "watch clouds", "drink water"]

print(task_list)

```
Save again command and s

Great, done, but why isn't the list printing out? Because we have not run the file. We will do this within the VSC terminal. Using the shortcut "control + backtick" the terminal will open in VSC directly or you can use the general terminal window we created the file within in the first place, you just need to ensure you're within your working folder where the lists.py file is saved.

We will type "python3" , which tells your computer to to interpret your file with python3 and then the file name.

```python
#Terminal

python3 task_list
```
Then hit enter and your list will be printed out within terminal.

```python
#Terminal

['eat pie', 'watch clouds', 'drink water']
```

# Index

Lists are used to collate objects together as a collection but how do we access those objects within our list? Well, this is where the ordered aspect of lists comes in. Lists are indexed, they are numbered and you can access what's written in the list at each index point so they are stored and saved in the order initialised and they cannot be shuffled around. Think less of a loose bag jostling your items around and more of a filing cabinet, with separate files containing the objects.

To reference the index point and therefore the object stored at that index we use the variable name followed by opening square bracket and the index number for it but importantly, indexes start at 0.


```python
# lists.py

...

print(task_list[0])
# returns--> eat pie

```

If we look at a storage container, this is our list
| eat pie | watch clouds | drink water |
                            

If we want to access the initial object we want to access the first memory address, this first address is by default 0, after which is the first derivative and the second derivative.
| eat pie | watch clouds | drink water |
     ^           1              2

You can also access items from the end of the list by using a negative index.
To get drink water we'd write

```python
#lists.py

print(task_list[-1])
```
once we save and run the file again you should see 'drink water' appear.

# Importantly
Lists have their limits, if you don't know the index of the object you are searching for you will have to go through the entire collection to find it.


# From the index we can alter or update an object by reassigning it

To change 'eat pie' to eat cake we need to reassign the task_list[0] and to do this we type

```python
#lists.py

task_list = ["eat pie", "watch clouds", "drink water"]

task_list[0] = "eat cake"

```
save the file and run it in the terminal
Note how the previous prints returned the objects assigned to the original task_list and it's only once reassigned that task_list[0] prints out as the new objects and has been reassigned. This is because Python code is run from top to bottom.

# Adding objects in a list

To add an object we use the append method and as I'm noticing now I've actually forgotten to include an incredbily important task to my to do list: day-dream. To do this we call the list variable, the append method involves writing ".append()" and within the brackets we put the object we want to add to the list. 
Append will always add items to the end of our list.

```python
#lists.py

task_list = ["eat pie", "watch clouds", "drink water"]

task_list.append("day-dream")

```
Save the file and let's run the code in the terminal 

```python

python3 lists.py

```
# Removing items from a list

To remove an item we use the pop method. I've realised that I don't actually want day-dream on my task list so let's remove day-dream by using the pop() method.

```python
#lists.py

task_list = ["eat pie", "watch clouds", "drink water"]

task_list.append("day-dream")

```
Similarly to the append() method pop() can only remove the last item in a list.


# To find out the length of a list
We use the len() function. 

```
tasks_num = task_list.len()

print(tasks_num)
```


# An Introduction to Lists

**10-15 minutes**

Hello there, today we are looking at and understanding Python Lists, our learning objectives for this speedy run-down are... 

### Learning Objectives
 - Understand the general concept of what a list is
 - Create a list
 - Access an element in a list.
 - Alter list items by 
    - Changing them/ reassigning them
    - Adding items
    - Removing items
- Access information regarding our list such as
    - Length of the list


To start with, let's get to grips with what a list actually is:

A list, as I'm sure you are aware in general is a group of elements/ objects. A list is a collection, be that your favourite holiday destinations, most delicious snacks, or a task list for instance.

And a Python list is just that, it is a mutable, ordered data structure, a collection of objects, stored under one variable, a name.

For instance that Task List could consist of

Task List
- eat pie
- watch clouds
- drink water

and anything else you have planned for the day. This list of elements is stored or contained under the name, or variable of Task List. 


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

## Onto Lists!

We start by giving our list a name and because you cannot use spaces within variables we will follow convention and use an underscore to separate the words. 

There are other naming conventions but this is not important right now.
In our file We will type task_list


```python
# lists.py

task_list
```

To relate our list items to their variable we use the assignment operator: "="

```python
# lists.py

task_list = 
```

And then we add our items, in Python this requires using square brackets - almost like the edges of our container.

```python
# lists.py

task_list = []
```

## Objects

When adding the objects to our list we separate them with commas and due to the objects consisting of strings we will need to contain them in quotation marks:

```python
# lists.py

task_list = ["eat pie", "watch clouds", "drink water"]
```

And then we'll save it!

## Now What
So we've created a beautiful list and we can check it exists under task_name by adding a return statement, so the list is actually returned to us. To do this we will use the print function. This is a built in function of Python and prints whatever you specify.

```python
# lists.py

task_list = ["eat pie", "watch clouds", "drink water"]

print(task_list)

```
Save again with command and s

Great, done, so... where is it printing out? Is it printing out? No, because we have not run the file. 
To run the file we will use the VSC terminal. Using the shortcut "control + backtick" the terminal will open in VSC directly or you can use mac terminal where we created the file in the first place, you just need to ensure you're within your working folder where that file exists.

In terminal we will type "python3" , which tells your computer to interpret your file with python and then the file name.

```python
#Terminal

python3 task_list
```

Then hit enter and your list should be printed out within terminal.


```python
#Terminal

['eat pie', 'watch clouds', 'drink water']
```

# Index

Lists are used to collate objects together as a collection but how do we access those objects within our list? Well, this is where the ordered aspect of lists comes in. Lists are indexed, they are numbered and you can access what's written in the list at each index point. 

List items are stored and saved in the order initialised and they cannot be shuffled around. Think less of a loose bag jostling your items and more of a filing cabinet, with separate files containing the objects.

To reference the index point and therefore the object stored at that index we use the variable name followed by an opening square bracket and the index number for said object but importantly, indexes start at 0. Which I will explain further but first let's see it in practice. 


```python
# lists.py

...

print(task_list[0])
# returns--> eat pie

```

# What's the deal with zero?

If we look at a storage container, this is our list

| eat pie | watch clouds | drink water |
                            

If we want to access the initial object we want to access the first memory address, which is by default 0, after which is the first derivative and the second derivative.

Another way to think of it is, if we want to access the first memory address we don't want to go anywhere, we don't want to move a space so we start at 0. If we want "watch clouds" we move 1 space to index 1 and so on. 

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


# Editing/ changing the objects

We edit or change an object using the index, to change 'eat pie' to 'eat cake' we need to reassign the the 0 index and to do so we type 

```python
#lists.py

...

task_list[0] = "eat cake"

```

And we want to print this new list out so we add a print statement again.

```python
#lists.py

...

print(task_list)

```

save the file and run it in the terminal, hit the up arrow then enter

Note how the previous prints returned the objects assigned to the original task_list and it's only the print statement after reassigning that returns our edited list. 

This is because Python code is run from top to bottom.


# Adding objects in a list

To add an object we use the append method and as I'm noticing now I've actually forgotten to include an incredbily important task to my to do list: day-dream. 

First we will write the list variable because the list is where we want to add the item to, then call the append method ".append()" and within the brackets we put the object we want to add to the list. Again, because it's a string we must use quotation marks.

Append will always add items to the end of our list.

```python
#lists.py
...
task_list.append("day-dream")

```
Save the file and let's run the code in the terminal 

```python

python3 lists.py

```

Oh but wait, why can't we see our latest edition to our list? Because we didn't add a print statement so the code didn't know to return anything to us. Let's do that now.

```python
#lists.py

print(task_list)

```

# Removing items from a list

To remove an item we use the pop method. How convenient that I actually don't want day-dream on my task list so let's remove it using the pop() method.

Similarly to the append() method pop() can only remove the last item in a list so it doesn't need anything written in the brackets.

```python
#lists.py

task_list.pop()

print(task_list)

```


# To find out the length of a list
We use the len() function, to do so we write len() with task_list as its parameter and then in order to return this so we can see the length we'll save it to a variable and then print it out.

```
tasks_num = len(task_list)

print(tasks_num)
```

# Recap

So what have we learned?

We know what a list is, we know how to create a list with objects, we know how to access an individual item in the list, how to edit, add and remove objects from a list and how to get the length of a list. There are a number of methods that come built in with lists and I'd recommend having a look through them, just to familiarise yourself with the possibilities.

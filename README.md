# Introduction-to-Python
Data Science Journey Re-Start

# General purpose programming language
# Open source
# You can do so many things with Python!
# Python shell is where you can do Python codes
# Interactive Python is part of the broader Jupyter ecosystem
# Python script are text files - .py

# Python is a great calculator
# Variables have specific case-sensitive name
# Creating variables helps with reproducibility
height = 1.79
weight = 68.7
height # output is 1.79
bmi = weight/height **2
bmi # output is 21.4413

# Python types
type(bmi) # says its a 'float'
day_of_week = 5
type(day_of_week) # says its "int"
x = 'body mass index'
y = 'this works too'
# ^this is called a string, you use quotes
type(y) # outputs str
z=True
type(z) # outputs bool (True/False)
# strings are particularly good when you need to filter

2 + 3
# 5

'ab' + 'cd'
# 'abcd'

# how the code behaves on the types of variables
# float, or floating point: a number that has both an integer and fractional part, separated by a point. 1.1, is an example of a float.

# Python Lists
# you use square brackets
# can use all Python types in the same list
[a,b,c]
fam = ['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89]
fam2 = [['liz',1.73], ['emma',1.68],['mom',1.71],['dad',1.89]]
# fam2 contain little lists that are wrapped in square brackets and separated with commas

hall = 11.25
kit = 18.0
liv = 20.0
bed = 10.75
bath = 9.50

# Create list areas
areas = [hall, kit, liv, bed, bath]

# Print areas
print(areas)
[11.25, 18.0, 20.0, 10.75, 9.5]

hall = 11.25
kit = 18.0
liv = 20.0
bed = 10.75
bath = 9.50

# Adapt list areas
areas = ["hallway", hall, "kitchen", kit, "living room", liv, "bedroom", bed, "bathroom", bath]

# Print areas
print(areas)
['hallway', 11.25, 'kitchen', 18.0, 'living room', 20.0, 'bedroom', 10.75, 'bathroom', 9.5]

hall = 11.25
kit = 18.0
liv = 20.0
bed = 10.75
bath = 9.50

# House information as list of lists
house = [["hallway", hall],
         ["kitchen", kit],
         ["living room", liv],
         ["bedroom", bed],
         ["bathroom",bath]]

# Print out house
print(house)
[['hallway', 11.25], ['kitchen', 18.0], ['living room', 20.0], ['bedroom', 10.75], ['bathroom', 9.5]]

# Subsetting Lists
fam = ['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89]
fam[3]
# outputs 1.68

fam[6]
# outputs 'dad'

# Python uses 0 indexing
# you can use negative indexing
# fam[6] and fam[-1] will produce 'dad' and 1.89
# fam[-1] and fam[7] will produce the same 1.89 result

# Slicing can create new lists
fam = ['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89]
fam[3:5] # outputs 1.68 and 'mom'
# ^only elements 3 and 4 are included
# [start (inclusive : end (exclusive)]

# Subsetting lists of lists
house = [["hallway", 11.25],
         ["kitchen", 18.0],
         ["living room", 20.0],
         ["bedroom", 10.75],
         ["bathroom", 9.50]]

# Subset the house list
# the first bracket refers to the list within the larger list, the second brackets refers to the elements within that list that is within the larger list
house[-1][1]
9.5

# List Manipulation
# Changing list elements
fam = ['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89]
fam[7] = 1.86
fam
# output is ['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.86]
# 1.89 is changed to 1.86

fam[0:2] = ['lisa',1.74]
fam
# output is ['lisa',1.74,'emma',1.68,'mom',1.71,'dad',1.86]
# first two elements [0:2] were changed

# Adding and removing elements
fam + ['me',1.79]
# ['lisa',1.74,'emma',1.68,'mom',1.71,'dad',1.86, 'me', 1.79]
fam_ext = fam + ['me', 1.79]
del fam[2]
# deletes 'emma' from list

# Behind the Scenes
x = ['a','b','c']
# you're storing your list in your computer memory and store the 'address' of that list in x
# x does not contain list elements, rather, it contains a reference to the list
# make a copy of the list x and call it y
y=x
# change an element in the y list (a copy of x)
y[1] = 'z'
y
['a','z','c']
# notice that the element also changes in x. why?
x
['a','z','c']
# because when you copy x to y, you copy the reference of this, not the actual value itself
# when you're updating an element in the list, it is one in the same list in the computer memory you are changing
# both x and y point to this list, so the update is visible from both variables
# if you want to create a list y that points to a new list in the memory with the same values, you need to use something other than the = sign
# you can use the list function
x = ['a','b','c']
y = list(x)
# or use a slice function to select all elements explicitly
# if we now make a change to the list y points to, x is not affected
y=x[:]
y[1]='z'
x
# outputs ['a','b','c']

# RECAP
# to replace list elements, you subset the list and assign new values to the subset
# you can select single elements or you can change entire list slices at once
# Create the areas list
areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

# Correct the bathroom area
areas[-1]=10.50
print(areas)

# Change "living room" to "chill zone"
areas[4]="chill zone"
print(areas)
['hallway', 11.25, 'kitchen', 18.0, 'living room', 20.0, 'bedroom', 10.75, 'bathroom', 10.5]
['hallway', 11.25, 'kitchen', 18.0, 'chill zone', 20.0, 'bedroom', 10.75, 'bathroom', 10.5]

# Extending a list
# use the + operator
# Create the areas list and make some changes
areas = ["hallway", 11.25, "kitchen", 18.0, "chill zone", 20.0,
         "bedroom", 10.75, "bathroom", 10.50]

# Add poolhouse data to areas, new list is areas_1
areas_1 = areas + ["poolhouse",24.5]

# Add garage data to areas_1, new list is areas_2
areas_2 = areas_1 + ["garage",15.45]
print(areas_1)
print(areas_2)
['hallway', 11.25, 'kitchen', 18.0, 'chill zone', 20.0, 'bedroom', 10.75, 'bathroom', 10.5, 'poolhouse', 24.5]
['hallway', 11.25, 'kitchen', 18.0, 'chill zone', 20.0, 'bedroom', 10.75, 'bathroom', 10.5, 'poolhouse', 24.5, 'garage', 15.45]

# Deleting list elements
# use the del statement
# when you remove an element from a list, the indexes of the elements that come after the deleted element all change
areas = ["hallway", 11.25, "kitchen", 18.0,
        "chill zone", 20.0, "bedroom", 10.75,
         "bathroom", 10.50, "poolhouse", 24.5,
         "garage", 15.45]

# Delete the poolhouse items from the list
del areas[10:12]

# Print the updated list
print(areas)
['hallway', 11.25, 'kitchen', 18.0, 'chill zone', 20.0, 'bedroom', 10.75, 'bathroom', 10.5, 'garage', 15.45]

# Inner workings of lists
# in this example, areas and areas_copy both point to the same list
# therefore, when an element in one changes, the same element in the other changes as well
# if we want to prevent changes in areas_copy from also taking effect in areas, we will have to do a more explicit copy of the areas list with list() or by using [:]
# Create list areas
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Change this command
areas_copy = list(areas)
# Change areas_copy
areas_copy[0] = 5.0
# Print areas
print(areas)
print(areas_copy)
[11.25, 18.0, 20.0, 10.75, 9.5]
[5.0, 18.0, 20.0, 10.75, 9.5]

# Functions
# type() returns a type of a value
# a piece of reusable code aimed at a particular task
fam = [1.73, 1.68, 1.71, 1.89]
max(fam)
# output is 1.89
tallest = max(fam)

# round()
round(1.68,1)
# 1.7
round(1.68)
# 2
# ndigits is an optional argument

# help()

# Create variables var1 and var2
var1 = [1, 2, 3, 4]
var2 = True

# Print out type of var1
type(var1)
# says its a list

# Print out length of var1
len(var1)
# says the length is 4

# Convert var2 to an integer: out2
out2 = int(var2)
print(out2)
# says that 'True' is now an integer

?sorted
Signature: sorted(iterable, /, *, key=None, reverse=False)
Docstring:
Return a new list containing all items from the iterable in ascending order.

A custom key function can be supplied to customize the sort order, and the
reverse flag can be set to request the result in descending order.
Type:      builtin_function_or_method

# Create lists first and second
first = [11.25, 18.0, 20.0]
second = [10.75, 9.50]

# Paste together first and second: full
full = first + second

# Sort full in descending order: full_sorted
full_sorted = sorted(full, reverse = True)

# Print out full_sorted
print(full_sorted)
[20.0, 18.0, 11.25, 10.75, 9.5]

# Methods
# all types are objects
# a str, float, and list are all objects
# methods are functions that belong to objects
fam.index('mom') # 'call method index() on fam'
# python returns 4
fam = ['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89]
fam.count(1.73)
# python returns 1

# lists are not the only python objects that have methods associated
# str methods
# capitalize() returns a string where the first letter is capitalized now
sister
'liz'
sister.capitalize()
'Liz'

# replacing a string
sister.replace('z','sa')
'lisa'

# Method
# everything = object
# objects have methods associated, depending on type
# for example, strings have replace methods, but a list does not
# index method is available in string and list types
# some methods can change the objects they are called on
fam = ['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89]
fam.append('me')
['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89,'me']
fam.append(1.79)
['liz',1.73,'emma',1.68,'mom',1.71,'dad',1.89,'me', 1.79]

# Summary
type(fam)
# returns list
# methods: call functions on objects
fam.index('dad')
# returns 6


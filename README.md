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

# String Methods
# .upper() turns a string into all caps
# string to experiment with: place
place = "poolhouse"

# Use upper() on place
place_up = place.upper()

# Print out place and place_up
print(place)
print(place_up)
poolhouse
POOLHOUSE

# .count() returns the # of called items
# Print out the number of o's in place
print(place.count('o'))
3

# List Methods
# .index() method gets the index of the element in a list
# .count() methods gets the count of how many times an element appears in a list
# Create list areas
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Print out the index of the element 20.0
print(areas.index(20.0))

# Print out how often 9.50 appears in areas
print(areas.count(9.50))
2
1

# More List Methods
# .append() adds an element to the list it is called on
# .remove() removes the first element of a list that matches the input, and
# .reverse() reverses the order of the lements in the list it is called on
# Create list areas
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Use append twice to add poolhouse and garage size
areas.append(24.5)
areas.append(15.45)

# Print out areas
print(areas)

# Reverse the orders of the elements in areas
areas.reverse()

# Print out areas
print(areas)
[11.25, 18.0, 20.0, 10.75, 9.5, 24.5, 15.45]
[15.45, 24.5, 9.5, 10.75, 20.0, 18.0, 11.25]

# Packages
# functions and methods are powerful
# all code in Python distribution -> that would lead to a huge messy code base
# this is where packages come in
# Packages are a directory of python scripts
# each script = module
# packages specify functions, methods, types
# thousands of packages available such as NumPy and Matplotlib

# you must install packages first
# download get-pip.py
# terminal: python3 get-pip.py

# Import Package
import numpy
array([1,2,3])
numpy.array([1,2,3)]
# arrays have parenthesis around square brackets
# lists contain brackets only

# if you want, you can just select a particular function from a package
from numpy import array
array([1,2,3])
# but this can cause confusion especially if you are working in groups
# the standard is the following:
import numpy as np
np.array([1,2,3])

# Practice importing a package
# Import the math package
import math

# Calculate C
C = 2 * 0.43 * math.pi

# Calculate A
A = math.pi * 0.43 ** 2

print("Circumference: " + str(C))
print("Area: " + str(A))
Circumference: 2.701769682087222
Area: 0.5808804816487527

# selective importing
# Import pi function of math package
from math import pi

# Calculate C
C = 2 * 0.43 * pi

# Calculate A
A = pi * 0.43 ** 2

print("Circumference: " + str(C))
print("Area: " + str(A))
Circumference: 2.701769682087222
Area: 0.5808804816487527

# there are many ways to import packages and modules into Python
# depending on the import call, you'll have to use different Python code
# for ex., if you want to use the function inv(), which is in the linalg subpackage of the scipy package. You want to be able to use this function as follows:
from scipy.linalg import inv as my_inv
# ^ this allows you to use my_inv([[1,2], [3,4]])

# Lists Recap
# powerful
# collection of values
# holds different types
# change, add, remove
# need for data science though
# python cannot do calculations on lists
# the solution is NumPy

# NumPy
# numeric python
# alternative to python list: NumPy Array
# calculations over entire arrays
# easy and fast
# installation: pip3 install numpy

# turning the height list into an array
import numpy as np
np_height = np.array(height)
np_height
array([1.73, 1.68, 1.71, 1.89, 1.79)]
# turning the weight list into an array
np_weight = np.array(weight)
array([65.4, 59.2, 63.6, 88.4, 68.7])
bmi = np_weight/np_height ** 2
bmi
array([21.851, 20.975, 21.750, 24.747, 21.441])

# unlike lists, NumPy arrays only contain one data type
# some remarks
# different types will lead to different behaviors
python_list = [1,2,3]
numpy_array = np.array([1,2,3)]
python_list + python_list
[1,2,3,1,2,3]
numpy_array + numpy_array
array([2,4,6])

# NumPy subsetting
bmi
array([21.851, 20.975, 21.750, 24.747, 21.441])
bmi[1]
20.975
bmi > 23
array([False, False, False, True, False)]

# you can use this boolean array inside square brackets to do subsetting
# this creates a new array consisting of original elements, not True/False boolean elements
bmi[bmi > 23]
array([24.747])

# Import the numpy package as np
import numpy as np
baseball = [180, 215, 210, 210, 188, 176, 209, 200]

# Create a numpy array from baseball: np_baseball
np_baseball = np.array(baseball)

# Print out type of np_baseball
print(type(np_baseball))
<class 'numpy.ndarray'>

# note that for lists, there are commas separating each value
# there are no commas separating values in numpy arrays
print(baseball)
print(np_baseball)
[180, 215, 210, 210, 188, 176, 209, 200]
[180 215 210 210 188 176 209 200]

# Import numpy
import numpy as np

# Create a numpy array from height_in: np_height_in
np_height_in = np.array(height_in)

# Print out np_height_in
print(np_height_in)

# Convert np_height_in to m: np_height_m
np_height_m = np_height_in * 0.0254

# Print np_height_m
print(np_height_m)
[74 74 72 ... 75 75 73]
[1.8796 1.8796 1.8288 ... 1.905  1.905  1.8542]

# numpy is great for doing vector arithmetic
# if you try to mix types in numpy arrays, like booleans and integers, numpy converts them to a common type
# Booleans like True and False are treated as 1 and 0 when combined with numbers, so the arrays ends up as integers
# also, arithmetic operators such as +, -, * and / have a different meaning for regular Python lists and numpy arrays

# subsetting numpy arrays
# subsetting (using [] notation on lists or arrays) works exactly the same with both lists and arrays
import numpy as np

np_weight_lb = np.array(weight_lb)
np_height_in = np.array(height_in)

# Print out the weight at index 50
print(np_weight_lb[50])

# Print out sub-array of np_height_in: index 100 up to and including index 110
print(np_height_in[100:111])
200
[73 74 72 73 69 72 73 75 75 73 72]

# 2D NumPy Arrays
# type of NumPy Arrays
import numpy as np
np_height = np.array([1.73, 1.68, 1.71, 1.89, 1.79)]
np_weight = np.array([65.4, 59.2, 63.6, 88.4, 68.7])
type(np_height)
# ^result will be 'numpy.ndarray'
type(np_weight)
# ^result numpy.ndarray
# the arrays np_height and np_weight are 1D arrays, but you can create 2D, 3D, 4D etc arrays

# 2D NumPy Arrays
np_2d = np.array([[1.73, 1.68, 1.71, 1.89, 1.79], 
                  [65.4, 59.2, 63.6, 88.4, 68.7]])
np_2d
# ^result will be 'array([[1.73, 1.68, 1.71, 1.89, 1.79], 
                          [65.4, 59.2, 63.6, 88.4, 68.7]])'

np_2d.shape
(2, 5) # 2 rows, 5 columns
# shape is the so-called attribute of the np2d array, that can give you info of what the data structure looks like
# note that the syntax for accessing an attribute looks a bit like calling a method, but they are NOT the same
# recall that methods have round brackets after them, attributes do not

# for 2D arrays, the NumPy rule applies: an array can only contain a single type!
# if you change the type of one, all the other elements will become that type now
# you can think of a 2D NumPy array as an improved list of lists

# Subsetting 2D NumPy Arrays
         0     1     2     3     4
array([[1.73, 1.68, 1.71, 1.89, 1.79],    0
       [65.4, 59.2, 63.6, 88.4, 68.7]])   1

# to select an entire row:
np_2d[0]
array([1.73, 1.68, 1.71, 1.89, 1.79])

# to select a specific element, select the row and then the column in that row:
np_2d[0][2]
1.71

# another way to subset to get the same value as the one above:
np_2d[0,2]
1.71
# the value before the comma specifies the row
# the value after the comma specifies the column
# the intersection is returned

# using the height and weight example
         0     1     2     3     4
array([[1.73, 1.68, 1.71, 1.89, 1.79],    0
       [65.4, 59.2, 63.6, 88.4, 68.7]])   1

# if you only want the second and third columns, put in indices 1 to 3 after the comma:
np_2d[:, 1:3]
array([[1.68, 1.71],
       [59.2, 63.6]])

import numpy as np

baseball = [[180, 78.4],
            [215, 102.7],
            [210, 98.5],
            [188, 75.2]]

# Create a 2D numpy array from baseball: np_baseball
np_baseball = np.array(baseball)

# Print out the type of np_baseball
print(type(np_baseball))

# Print out the shape of np_baseball
print(np_baseball.shape)
<class 'numpy.ndarray'>
(4, 2)

import numpy as np

# Create a 2D numpy array from baseball: np_baseball
np_baseball = np.array(baseball)

# Print out the shape of np_baseball
print(np_baseball.shape)
(1015, 2)

# Subsetting 2D NumPy Arrays
# if the 2D numpy array has a regular structure (each row and column has a fixed # of values) subsetting becomes easy.
# indexes before the comma refer to the rows, while those after the comma refer to the columns
# the : is for slicing; this this example, it tells Python to include all rows
import numpy as np
np_x = np.array(x)
np_x[:, 0]

import numpy as np
np_baseball = np.array(baseball)

# Print out the 50th row of np_baseball
print(np_baseball[49,:])

# Select the entire second column of np_baseball: np_weight_lb
np_weight_lb = (np_baseball[:,1])
print(np_weight_lb)

# Print out height of 124th player
print(np_baseball[123])
[ 70 195]
[180 215 210 ... 205 190 195]
[ 75 200]

# both of these print out the 50th row ([ 70 195]) of np_baseball 
print(np_baseball[49,:])
print(np_baseball[49])

# Select the entire second column of np_baseball: np_weight_lb
# recall that the shape of np_baseball is 1015 rows and 2 columns
np_weight_lb = (np_baseball[:,1])
print(np_weight_lb)
[180 215 210 ... 205 190 195]

# note that below doesn't yield a result
np_weight_lb_2 = (np_baseball[,1])
print(np_weight_lb_2)
  File "<script.py>", line 1
    np_weight_lb_2 = (np_baseball[,1])
                                  ^
SyntaxError: invalid syntax

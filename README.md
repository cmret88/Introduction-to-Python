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

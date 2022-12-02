##### Name: Jane Shin 
##### Date: December 1, 2022 
##### Course: IT FDN 110 A Au 22: Foundations of Programming: Python


# Assignment 07 – Files & Exceptions


## Introduction 
This document describes the steps taken in performing Assignment 07, where a Python script file from Assignment 06 is updated to demonstrate the concepts of exception handling and pickling module.

The script still uses a printed "menu" to guide the user through various options for the “To-do List”, including displaying current list, adding a new item, removing an existing item, saving data to the original file, and exiting the program.  The scope of work is similar to that of Assignment 06, and uses functions and classes to organize Data, Processing, and Presentation sections.  However, it uses pickling modules to read and write to files, and has a structured error handling feature.

The "To-do List" file contains two columns of data, "Task" and "Priority."  The columns are loaded into a Python dictionary object.  Each dictionary object represents one row of data, and these rows are added to a Python list object to create a table of data.

New tools and concepts introduced in Module 7, such as, pickling modules and a structured error handling feature, as well as previously addressed concepts such as list, dictionary, functions and classes will be used in accomplishing this task. 


## Instructions 
Module 7 covered a detailed application of the function and class concepts, delivered through course videos, a book chapter, and web pages.  The course material delivered detailed explanation and examples of the following topics: 

•	Working with text files – Read, Append modes 

•	Options for reading data  

•	Combining reading and writing	 

•	Working with binary files, using pickling modules

•	Structured error handling (Try-Except)	

•	Using the exception class	

•	Catching specific exceptions	

•	Raising custom errors	

•	Creating custom exception classes	

•	Creating GitHub pages and a markdown file, formatting the page 
  
 
## Research Exception Handling in Python
Helpful websites		 

https://www.learnpython.org/en/Exception_Handling 

https://pythonbasics.org/try-except/ 

These websites had thorough explanations on the concept of error handling, the reason why it is needed, and practical examples of errors and potential handling suggestions for them.


## Research Pickling in Python
Helpful website		

https://docs.python.org/3/library/pickle.html  

In addition to an overview with short examples, it provided a link to the GitHub page with a source code to review, which helped with a more holistic understanding of the concept and application.


## Creating the Script - Header and Initial Comments  

```
# ---------------------------------------------------------------------------- #
# Title: Assignment 07
# Description: Working with functions in a class,
#              When the program starts, load each "row" of data
#              in "ToDoList.dat" into a python Dictionary.
#              Add each dictionary "row" to a python list "table"
#              New for Assignment 07
#               - Provide user feedback on expected errors using structured error handling
#               - Read and save a binary file using a technique called pickling
# ChangeLog (Who,When,What):
# RRoot,1.1.2030,Created started script
# JShin,11.23.2022,Modified code to complete assignment 06
# JShin,11.30.2022,Modified code to complete assignment 07, Renamed the file as Assignment07.py
# ---------------------------------------------------------------------------- #
```

•	PyCharm was used to create and run the script.  The assignment was saved as a .py file named “Assignment07.py” at the location according to a direction given in the instruction.  

•	Script header and comments – A script header was created per the examples given in the instruction to communicate the function and document changes of the script.

•	The Change Log was updated to reflect the codes added to the original starter script to complete the assignment.


## Declaration of Variables
```
# Data ---------------------------------------------------------------------- #
# Declare variables and constants
file_name_str = "ToDoList.dat"  # The name of the data file
file_obj = None  # An object that represents a file
row_dic = {}  # A row of data separated into elements of a dictionary {Task,Priority}
table_lst = []  # A list that acts as a 'table' of rows
choice_str = ""  # Captures the user option selection
task_str = ""  # Captures the task input from functions to be processed in main body
priority_str = ""   # Captures the priority input from functions to be processed in main body
```

•	Using the “Separation of Concerns” concept, variables and constants are declared within the “Data” section along with comments explaining the purposes of each variable.  

•	Variables are organized in order of appearance.

•	Variable from the original script were retained, and several new variables were added.

•	The value of file_name_str was updated to “ToDoList.dat” to be used with pickling module.


## Overall Script Structure 



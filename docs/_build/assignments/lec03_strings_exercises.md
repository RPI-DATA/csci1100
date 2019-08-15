---
redirect_from:
  - "/assignments/lec03-strings-exercises"
interact_link: content/C:\Users\sjgar\Documents\GitHub\csci1100\docs\content\assignments/lec03_strings_exercises.ipynb
kernel_name: python3
has_widgets: false
title: 'Assignment 2'
prev_page:
  url: /assignments/lec02_calculator_exercises
  title: 'Assignment 1'
next_page:
  url: /assignments/lec04_modules_functions1_exercises
  title: 'Assignment 3'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


Notebook created: 2019-07-16 14:30:27  
Generated from: jWebsite/lecture_notes/lec03_strings_exercises/exercises.rst  



# Lecture 3 - Exercises



## Overview

Solutions to the problems below must be sent to Submitty for grading.
A separate file must submitted for each problem, as practiced in
Lab 1.  For these Lecture 3 exercises, you must submit your
solutions before Wednesday, September 13 at 11:59:59. Starting with Lecture 4,
you will be required to submit you lecture exercises within 24 hours
of the end of lecture.  Students are
welcome to work on these problems in small groups, but each student
should write the final version of their solutions independently to
assure themselves that they understand.



## Problems

1. Which of the following are valid strings?  Upload a text file to
Submitty that contains just the variable names that are assigned to
strings that are correct.  For example if only the first two were
correct your file would contain s0 on the first line and s1 on the
second.  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s0 = "Sheldon Cooper's apartment is in Pasedena"

>>> s1 = 'This cheese shop's cheese is all gone"

>>> s2 = """We are
"The Knights of the Round Table"
"""

>>> s3 = "Toto, I said,\n"We aren't in Kansas, anymore!"


>>> s4 = 'Have you seen the "Final Five"'s picture?'


>>> s5 = "Have you seen the 'Final Five''s picture?"

```
</div>

</div>



1. Submit a Python file that includes a single line of code that prints
  25 `'*'` characters followed by 25 `'+'` characters, with no
  space in between.  It must, of course, use the `print` function.
  The two characters must appear in your code *much less* than 25
  times - at most three each!  
1. Write a program that assigns the value 4 to the variable `x`, the
  value 2 to the variable `y` and then uses exactly *three*
  `print` function calls to generate the output below (four lines,
  with the second line blank).  The `print` calls must use the
  variables `x` and `y` rather than the values 4 and 2.  The
  trick is to change the assignment of the `sep` and `end`
  parameters in the call to `print`.  The character `4` is the
  first character on the 1st, 3rd and 4th lines of output.  


> 



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
4 2

4,2
42

```
</div>

</div>


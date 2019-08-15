---
redirect_from:
  - "/assignments/lec04-modules-functions1-exercises"
interact_link: content/C:\Users\sjgar\Documents\GitHub\csci1100\docs\content\assignments/lec04_modules_functions1_exercises.ipynb
kernel_name: python3
has_widgets: false
title: 'Assignment 3'
prev_page:
  url: /assignments/lec03_strings_exercises
  title: 'Assignment 2'
next_page:
  url: /grading
  title: 'Grading'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


Notebook created: 2019-07-16 14:30:27  
Generated from: jWebsite/lecture_notes/lec04_modules_functions1_exercises/exercises.rst  



# Lecture 4 - Exercises

Solutions to the problems below must be sent to Submitty for grading.
A separate file must submitted for each problem.  These must be
submitted by 4 pm on Tuesday, January 30.

1. Write a program that assigns a string to the variable called
`phrase` and then transforms `phrase` into a hashtag.  In other
words, all words in `phrase` are capitalized, all spaces are
removed, and a `#` appears in front.  Store the result in a
variable called `hashtag`.  Then print the value of both
`phrase` and `hashtag`.  Your program should start with  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
phrase = 'Things you wish you knew as a freshman'

```
</div>

</div>



and the output from the program (using `print()` function
calls) should be  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
The phrase "Things you wish you knew as a freshman"
becomes the hashtag "#ThingsYouWishYouKnewAsAFreshman"

```
</div>

</div>



Note that the output includes the quotation marks.  
1. One of the challenges of programming is that there are often many
ways to solve even the simplest problem.  Consider computing the
area of the circle with the standard formula  
$$
a(r) = \pi r^2
$$
Fortunately, we now have `pi` from the *math* module, but to
compute the square of the radius we now can use `**` or
`pow()` or we can just multiply the radius times itself.  To
print the area accurate to only a few decimal places we can now use
the string `format()` method or the `round()` built-in
function, which includes an optional second argument to specify the
number of decimal places.  
Write a short Python program that computes and prints the areas of
two circles, one with radius 5 and the other with radius 32.  Your
code must use `**` once and `pow()` once and it must use
`format()` once and `round()` once.  The output should be
exactly  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
Area 1 = 78.54
Area 2 = 3216.99

```
</div>

</div>


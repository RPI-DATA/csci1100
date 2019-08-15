---
redirect_from:
  - "/notebooks/lec03-strings"
interact_link: content/C:\Users\sjgar\Documents\GitHub\csci1100\docs\content\notebooks/lec03_strings.ipynb
kernel_name: python3
has_widgets: false
title: 'Lecture 3 - Python Strings'
prev_page:
  url: /notebooks/lec02_calculator
  title: 'Lecture 2 - Python as a Calculator'
next_page:
  url: /notebooks/lec04_modules_functions1
  title: 'Lecture 4 - Using Functions and Modules'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


Notebook created: 2019-07-16 14:30:27  
Generated from: jWebsite/lecture_notes/lec03_strings.rst  



# Lecture 3 - Python Strings



## Reading

This material is drawn from Chapter 4 of *Practical Programming*, 2nd
edition.



## More Than Just Numbers

- Much of what we do today with computers revolves around text:  
  - Web pages  
  - Facebook  
  - Text messages  
  These require working with *strings*.  
- Strings are our third type, after integers and floats.  
- We've already seen the use of strings in output,  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print("Hello world")
x = 8
y = 10
print("Value of x is", x, "value of y is", y)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
Hello world
Value of x is 8 value of y is 10
```
</div>
</div>
</div>





## Topics for Today

- String basics  
- String operations  
- Input to and output from your Python programs  



## Strings - Definition

- A string is a sequence of 0 or more characters delimited by single
quotes or double quotes.  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
'Rensselaer'
"Albany, NY"
'4 8 15 16 23 42'
''

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
''
```


</div>
</div>
</div>



- We can print strings:  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> print("Hello, world!")
#Hello, world!

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
Hello, world!
```
</div>
</div>
</div>



- Strings may be assigned to variables:  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s = 'Hello'
>>> t = "Good-bye"
>>> print(s)
Hello
>>> t
'Good-bye'

```
</div>

</div>



- Notice that unlike integers and floats there is now a difference
  between asking the Python function `print` to output the variable
  and asking the Python interpreter directly for the value of the
  variable.  



## Combining Single and Double Quotes in a String

- A string that starts with double quotes must end with double quotes,
  and therefore we can have single quotes inside.  
- A string that starts with single quotes must end with single quotes
  and therefore we can have double quotes inside.  
- To illustrate this, we will take a look at  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s = 'He said, "Hello, World!"'
>>> t = "Many single quotes here '''''''  and here ''' but correct."

```
</div>

</div>





## Multi-Line Strings

- Ordinarily, strings do not extend across multiple lines, causing an
  error if you try.  
- But, starting and ending a string `"""` or `'''` tells Python to
  allow the string to cross multiple lines.  
  - Any character other than `'''` (or `"""`, if that is how the
    string started) is allowed inside the string.  
- Example,  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s1 = """This
is a multi-line
string."""
>>> s1
'This\nis a multi-line\nstring.'
>>> print s1
This
is a multi-line
string.
>>>

```
</div>

</div>



- Notice the `\n` when we ask Python for the value of the string
  (instead of printing it). This is an *escape character*, as we will
  discuss next.  



## Escape Characters

- Inserting a `\` in the middle of a string tells Python that the
  next character will have special meaning (if it is possible for it to
  have special meaning).  
- Most importantly:  
  - `\n` - end the current line of text and start a new one  
  - `\t` - skip to the next 'tab stop' in the text. This allows
    output in columns  
  - `\'` - do not interpret the `'` as a string delimiter  
  - `\"` - do not interpret the `"` as a string delimiter  
  - `\\` - put a true back-slash character into the string  
- We'll explore the following strings in class  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s0 = "*\t*\n**\t**\n***\t***\n"
>>> s1 = "I said, \"This is a valid string.\""

```
</div>

</div>





## String Operations - Concatenation

- Concatenation: Two (or more) strings may be concatenated to form a
new string, either with or without the `+` operator. We'll look at  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s0 = "Hello"
>>> s1 = "World"
>>> s0 + s1
>>> s0 + ' ' + s1
>>> 'Good' 'Morning' 'America!'
>>> 'Good ' 'Morning ' 'America!'

```
</div>

</div>



- Notice that  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s0 = "Hello"
>>> s1 = " World"
>>> s0 s1

```
</div>

</div>



is a syntax error but  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> "Hello" " World"

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
'Hello World'
```


</div>
</div>
</div>



is not. Can you think why?  



## String Operations - Replication

- You can replicate strings by multiplying them by an integer:  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s = 'Ha'
>>> print(s * 10)
HaHaHaHaHaHaHaHaHaHa

```
</div>

</div>



- What do you think multiplying a string by a negative integer or 0
  does? Try it.  
- Many expressions you might try to write involving strings and either
ints or floats are illegal Python, including the following:  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> 'Hello' * 8.1
>>> '123' + 4

```
</div>

</div>



Think about why  



## Practice Problems - Part 1

We will go over these during lecture:

1. Which are valid Python strings:  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s1 = '"Hi mom", I said.  "How are you?"'
>>> s2 = '"Hi mom", I said.  '"How are you?"
>>> s3 = '"Hi mom", I said.  '"How are you?"'
>>> s4 = """'Hi mom", I said.  '"How are you?"'"""
>>> s5 = ""I want to be a lion tamer!"'
>>> s6 = "\"Is this a cheese shop?\"\n\t'Yes'\n\t\"We have all kinds!\""

```
</div>

</div>



For those that are not valid, what needs to be fixed?  For those
that are, what is the output when they are passed to the `print`
function?  
1. What is the output?  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s = "Cats\tare\n\tgood\tsources\n\t\tof\tinternet\tmemes"
>>> s
>>> print(s)

```
</div>

</div>



1. What is the output?  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print('\\'*4)
print('\\\n'*3)
print('Good-bye')

```
</div>

</div>



1. Which of the following are legal? For those that are, show what
Python outputs when these are typed directly into the interpreter.  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> 'abc' 'def'
>>> 'abc' + 'def'
>>> 'abc ' + 'def'
>>> x = 'abc'
>>> y = 'def'
>>> x+y
>>> x y
>>> s1 = 'abc'*4
>>> s1
>>> s2 = 'abc '*4
>>> print(s2)

```
</div>

</div>





## String Operations - Functions

- Python provides many operations for us to use in the form of
  **functions**.  We have already seen `print()`, but now we
  are going to look at other functions that operate on strings.  
- You can compute the length of a string with `len()`.  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> s = "Hello!"
>>> print(len(s))

```
</div>

</div>



- Here is what happens:  
  1. Function `len` is provided with the value of the string associated
    with variable `s`  
  1. `len` calculates the number of characters in the provided
    string using its own code, code that is *built-in* to Python.  
  1. `len` *returns* the calculated value (in this case, 6) and
    this value is sent to the `print` function, which actually
    generates the output.  
- We will learn more about using functions in Lectures 4 and 5.  



## Example String Functions

- We will look at examples of all of the following during lecture...  
- You can convert an integer or float to a string with `str()`.  
- You can convert a string that is in the form of an integer to an
  integer using `int()`  
- You can convert a string that is in the form of a float to a float
  using, not surprisingly, `float()`  



## The print Function in More Detail

- We already know a bit about how to use `print()`, but we can learn
about more using `help()`  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
help(print)
Help on built-in function print in module builtins:

print(...)
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)

    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.

```
</div>

</div>



- `flush` is useful when trying to debug. If you are trying to trace your
  program execution using print, adding `flush=True` as your final argument
  will give you more accurate results. We will talk about this more later.  
- For now, we will focus on the `sep` and `end` and illustrate with examples.  



## User Input

- Python programs can ask the user for input using the function called
  `input`.  
- This waits for the user to type a line of input, which Python reads
  as a string.  
- This string can be converted to an integer or a float (as long as it
  is properly an int/float).  
- Here is a toy example  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print("Enter a number")
x = float(input())
print('The square of', x, 'is', x*x)

```
</div>

</div>



- We can also insert the string right into the `input` function
call:  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
x = input("Enter a new number ")
x = float(x)
print('The square of', x, 'is', x*x)

```
</div>

</div>



- A similar function exists to convert a string to an integer:  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
x = input("Enter an integer ")
x = int(x)

```
</div>

</div>



- We will use this idea to modify our area and volume calculation so
  that the user of the program types in the numbers.  
  - The result is more useful and feels more like a real program
    (run from the command line).  
  - It will be posted on the course website.  



## Practice Problems - Part 2

1. What is the output for this Python program?  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(len('George'))
print(len(' Tom  '))
s = """Hi
sis!
"""
print(len(s))

```
</div>

</div>



1. Which of the following are legal? For those that are, show what
Python outputs when these are typed directly into the interpreter.  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
>>> 'abc' + str(5)
>>> 'abc' * str(5)
>>> 'abc' + 5
>>> 'abc' * 5
>>> 'abc' + 5.0
>>> 'abc' + float(5.0)
>>> str(3.0) * 3

```
</div>

</div>



1. What is the output of the following when the user types 4 when
running the following Python program?  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
x = input('Enter an integer ==> ')
x = x*2
x = int(x)
x *= 2
print("x is:", x)

```
</div>

</div>



1. What is the output when the user types the value 64 when running
the following Python program?  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
x = input('Enter an integer ==> ')
y = x // 10
z = y % 10
print(x, ',', y, z, sep='')

```
</div>

</div>



What happens when you do not have the call to the `int` function?  
1. Write a program that requests an integer from the user as an input
and stores in the variable `n`.  The program should then print
`n` 1's with 0's inbetween.  For example if the user input the
value 4 then the output should be  



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
1010101

```
</div>

</div>





## Summary

- Strings represent character sequences - our third Python type  
- String operations include addition (concatenate) and replication  
- Functions on strings may be used to determine length and to convert
  back and forth to integers and floats.  
- Escape sequences change the meaning of special Python characters or
  make certain characters have special meaning.  
- Some special characters of note: `\n` for new line, `\t` for tab.
  They are each preceded by `\`  
- The `print()` function offers significant flexibility.  
- We can read input using `input()`  


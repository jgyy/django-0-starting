# Training Python-Django - 0 Starting

**Summary**: Today, we'll embark on a journey to discover basics of the syntactics and semantics of Python.  
**Version**: 1

## Contents
1. [Preamble](#preamble)
2. [General rules](#general-rules)
3. [Today's specific rules](#todays-specific-rules)
4. [Exercise 00: My first variables](#exercise-00--my-first-variables)
5. [Exercise 01: Numbers](#exercise-01--numbers)
6. [Exercise 02: My first dictionary](#exercise-02-my-first-dictionary)
7. [Exercise 03: Key search](#exercise-03-key-search)
8. [Exercise 04: Search by value](#exercise-04-search-by-value)
9. [Exercise 05: Search by key or value](#exercise-05-search-by-key-or-value)
10. [Exercise 06: Dictionary sorting](#exercise-06-dictionary-sorting)
11. [Exercise 07: Periodic table of the elements](#exercise-07-periodic-table-of-the-elements)
12. [Submission and peer-evaluation](#submission-and-peer-evaluation)

## Preamble

The Zen of Python, by Tim Peters

```python
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea – let's do more of those!
```

```python
import this
```

## General rules

* Your project must be realized in a virtual machine.
* Your virtual machine must have all the necessary software to complete your project. These softwares must be configured and installed.
* You can choose the operating system to use for your virtual machine.
* You must be able to use your virtual machine from a cluster computer.
* You must use a shared folder between your virtual machine and your host machine.
* During your evaluations you will use this folder to share with your repository.
* Your functions should not quit unexpectedly (segmentation fault, bus error, double free, etc) apart from undefined behaviors. If this happens, your project will be considered non functional and will receive a 0 during the evaluation.
* We encourage you to create test programs for your project even though this work won't have to be submitted and won't be graded. It will give you a chance to easily test your work and your peers' work. You will find those tests especially useful during your defence. Indeed, during defence, you are free to use your tests and/or the tests of the peer you are evaluating.
* Submit your work to your assigned git repository. Only the work in the git repository will be graded. If Deepthought is assigned to grade your work, it will be done after your peer-evaluations. If an error happens in any section of your work during Deepthought's grading, the evaluation will stop.

## Today's specific rules

* No code in the global scope. We want functions!
* Each turned-in file must end with a function call in a condition identical to:
```python
if __name__ == '__main__':
    your_function(whatever, parameter, is, required)
```
* You can set an error management in this condition.
* No import will be authorized, except the ones explicitly mentioned in the 'Authorized functions' in each exercise's description.
* You won't have to manage the exceptions raised by the open function.
* You'll have to use the python3 interpreter.

## Exercise 00 : My first variables

**Turn-in directory**: `ex00/`  
**Files to turn in**: `var.py`  
**Allowed functions**: n/a

Create a script named `var.py` in which you will define a `my_var` function. In this function, you will declare 9 variables of different types and print them on the standard output. You will reproduce this output exactly:

```bash
$> python3 var.py
42 has a type <class 'int'>
42 has a type <class 'str'>
quarante-deux has a type <class 'str'>
42.0 has a type <class 'float'>
True has a type <class 'bool'>
[42] has a type <class 'list'>
{42: 42} has a type <class 'dict'>
(42,) has a type <class 'tuple'>
set() has a type <class 'set'>
$>
```

Of course, explicitly writing your variable types in the prints of your code is strictly prohibited. Don't forget to call your function at the end of your script as required by the instructions:

```python
if __name__ == '__main__':
    my_var()
```

## Exercise 01 : Numbers

**Turn-in directory**: `ex01/`  
**Files to turn in**: `numbers.py`  
**Allowed functions**: n/a

For this exercise, you're free to define as many function as you like and name them as you like also.

The `d01.tar.gz` tarball in the appendix of this subject contains a `ex01/` sub-folder that holds a `numbers.txt` file containing the numbers 1 to 100 separated by a coma. Design a Python script named `numbers.py` which role is to open a `numbers.txt` file, read the numbers it contains and display them on the standard output, one per line, without any coma.

## Exercise 02: My first dictionary

**Turn-in directory**: `ex02/`  
**Files to turn in**: `var_to_dict.py`  
**Allowed functions**: N.A.

Create a script named `var_to_dict.py` in which you will copy the following list of couples as is in one of your functions:

```python
d = [
    ('Hendrix' , '1942'),
    ('Allman' , '1946'),
    ('King' , '1925'),
    ('Clapton' , '1945'),
    ('Johnson' , '1911'),
    ('Berry' , '1926'),
    ('Vaughan' , '1954'),
    ('Cooder' , '1947'),
    ('Page' , '1944'),
    ('Richards' , '1943'),
    ('Hammett' , '1962'),
    ('Cobain' , '1967'),
    ('Garcia' , '1942'),
    ('Beck' , '1944'),
    ('Santana' , '1947'),
    ('Ramone' , '1948'),
    ('White' , '1975'),
    ('Frusciante', '1970'),
    ('Thompson' , '1949'),
    ('Burton' , '1939')
]
```

Your script must turn this variable into a dictionary. The year will be the key, the name of the musician the value. It must then display this dictionary on the standard output following a clear format:

```
1970 : Frusciante
1954 : Vaughan
1948 : Ramone
1944 : Page Beck
1911 : Johnson
...
```

The final order will not have to be the same as the example. This is a regular behavior. Do you know why?

## Exercise 03: Key search

**Turn-in directory**: `ex03/`  
**Files to turn in**: `capital_city.py`  
**Allowed functions**: `import sys`

Here are dictionaries you have to copy unaltered in one of your script's functions:

```python
states = {
    "Oregon" : "OR",
    "Alabama" : "AL",
    "New Jersey": "NJ",
    "Colorado" : "CO"
}

capital_cities = {
    "OR": "Salem",
    "AL": "Montgomery",
    "NJ": "Trenton",
    "CO": "Denver"
}
```

Write a program that takes a state as an argument (ex: Oregon) and displays its capital city (ex: Salem) on the standard output. If the argument doesn't give any result, your script must display: Unknown state. If there is no argument - or too many - your script must no do anything and quit.

```bash
$> python3 capital_city.py Oregon
Salem
$> python3 capital_city.py Ile-De-France
Unknown state
$> python3 capital_city.py
$> python3 capital_city.py Oregon Alabama
$> python3 capital_city.py Oregon Alabama Ile-De-France
$>
```

## Exercise 04: Search by value

**Turn-in directory**: `ex04/`  
**Files to turn in**: `state.py`  
**Allowed functions**: `import sys`

You get the same dictionaries as in the previous exercise. You have to copy them unaltered again in one of the functions of your script.

Create a program that takes the capital city for argument and displays the matching state this time. The rest of your program's behaviors must remain the same as in the previous exercise.

```bash
$> python3 state.py Salem
Oregon
$> python3 state.py Paris
Unknown capital city
$> python3 state.py
$>
```

## Exercise 05: Search by key or value

**Turn-in directory**: `ex05/`  
**Files to turn in**: `all_in.py`  
**Allowed functions**: `import sys`

Starting with the same dictionaries, you must copy them unaltered again in one of your script functions, and write a program that behaves as follows:

* The program must take for argument a string containing as many expressions as we search for, separated by a coma.
* For each expression in this string, the program must detect if it's a capital, a state or none of them.
* The program must not be case-sensitive. It must not take multiple spaces in consideration either.
* If there is no parameter or too many parameters, the program doesn't display anything.
* When there are two successive comas in the string, the program doesn't display anything.
* The program must display results separated by a carriage return and strictly use the following format:

```bash
$> python3 all_in.py "New jersey, Tren ton, NewJersey, Trenton, toto, , sAlem"
Trenton is the capital of New Jersey
Tren ton is neither a capital city nor a state
NewJersey is neither a capital city nor a state
Trenton is the capital of New Jersey
toto is neither a capital city nor a state
Salem is the capital of Oregon
$>
```

## Exercise 06: Dictionary sorting

**Turn-in directory**: `ex06/`  
**Files to turn in**: `my_sort.py`  
**Allowed functions**: N.A.

Integrate this dictionary in either function of yours as:

```python
d = {
    'Hendrix' : '1942',
    'Allman' : '1946',
    'King' : '1925',
    'Clapton' : '1945',
    'Johnson' : '1911',
    'Berry' : '1926',
    'Vaughan' : '1954',
    'Cooder' : '1947',
    'Page' : '1944',
    'Richards' : '1943',
    'Hammett' : '1962',
    'Cobain' : '1967',
    'Garcia' : '1942',
    'Beck' : '1944',
    'Santana' : '1947',
    'Ramone' : '1948',
    'White' : '1975',
    'Frusciante': '1970',
    'Thompson' : '1949',
    'Burton' : '1939',
}
```

Write a program that displays the names of the musicians sorted by year in ascending order, then in alphabetic order for similar years. One per line, without showing the year.

## Exercise 07: Periodic table of the elements

**Turn-in directory**: `ex07/`  
**Files to turn in**: `periodic_table.py`  
**Allowed functions**: `import sys`

The `d01.tar.gz` tarball in the appendix of this subject contains the `ex07/` sub-folder in which you'll find the `periodic_table.txt` file, that describes a periodic table of the elements in a format made for programmers.

Create a program that uses the file to write a HTML page representing the periodic table of the elements in a proper format.

* Each element must be in a 'box' of a HTML table.
* The name of an element must be in a level 4 title tag.
* The attributes of an element must appear as a list. The lists must state at least the atomic numbers, the symbol and the atomic mass.
* You must at least abide to the layout of the Mendeleiev's Table as it appears on Google. There must be empty boxes where there should, as well as carriage return where it should.

Your program must create the result file `periodic_table.html`. Of course, this HTML file must be readable in any browser and must be W3C valid.

You're free to design your program as you like. Don't hesitate to fragment your code in specific functionalities you may reuse. You can customize the tags with a CSS "inline" style to make your turn-in prettier (think of the table's borders' colors). You can even generate `periodic_table.css` file if you prefer.

Here is an excerpt of an output example that will give you an idea:

```html
[...]
<table>
<tr>
<td style="border: 1px solid black; padding:10px">
<h4>Hydrogen</h4>
<ul>
<li>No 42</li>
<li>H</li>
<li>1.00794</li>
<li>1 electron</li>
<ul>
</td>
[...]
```

## Submission and peer-evaluation

Turn in your assignment in your Git repository as usual. Only the work inside your repository will be evaluated during the defense. Don't hesitate to double check the names of your folders and files to ensure they are correct.

**The evaluation process will happen on the computer of the evaluated group.**

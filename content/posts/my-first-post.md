---
title: "My First Post"
date: 2020-02-29T13:22:32+08:00
draft: false
---

# Introduction to Jupyter Notebook

## What is Jupyter Notebook?

> The notebooks documents are documents produced by the Jupyter Notebook App, which can contain both code (e.g. Python) and rich text elements (paragraphs, equations, links, etc..).
> The Jupyter Notebook App is a client-server application that allows editing and running notebook documents by a browser.

Jypyter Notebook consists of two major types of cells: 

- **Markdown:** A cell that contains rich text elements.
- **Code:** A cell that contains Python codes, which you may run cell by cell. 

## Shortcuts 

- Shortcuts can help you to write a Jupyter Notebook more efficiently.
- Press `esc` then press `h` to show all shortcuts.

### Mac versus PC/Linux

| PC/Linux | Mac         |
| -------- | ----------- |
| `Ctrl`   | command `⌘` |
| `Shift`  | shift `⇧`   |
| `Alt`    | option `⌥`  |

### Two modes

- **Command mode**: convenient to move around/add/delete cells.
- To activate command mode, press `esc`.
- **Edit mode**: when you edit the cells.
- To activate edit mode, select a cell and double click or press `Enter`.

### Frequently used shortcuts **in command mode**

- `Shift + Enter`: run the current cell
- `Up` and `Down`: move up or down a cell
- `A`: insert cell above
- `B`: insert cell below
- `Y`: change the cell type to *Code*
- `M`: change the cell type to *Markdown*
- Press `D` twice: delete selected cells
- `Z`: undo cell deletion
- `S`: save
- `Shift + Up` and `Shift + Down`: extend selection by one cell
- `Ctrl + Enter`: run selected cell, when multiple cells are selected

### Frequently used shortcuts **in edit mode**

- `Tab`: code completion or indent
- `Ctrl + Z`: undo

# Rich text elements via Markdown

**Markdown** is a language that allow you to create rich text elements with plain-text-formatting syntax.

* Step 1: press the '+' button to create a cell
* Step 2: change the cell type to Markdown
* Step 3: write something in the cell
* Step 4: press `Shift + Enter`, after you finish the writting

### Headings

Use `#`s **followed by a blank space** for titles and section headings:

# H1

## H2

### H3

#### H4

##### H5

### Text formats

- *italics*, with `*asterisks*` or `_underscores_`.
- **bold**, with `**asterisks**` or `__underscores__`.
- **combined _emphasis_**, with `**asterisks and _underscores_**`.
- ~~Strikethrough~~, with two tildes `~~Scratch this~~`.

### Inline code

- Inline `code` has back-tick around `` ` `` it.
- Back-tick `` ` `` is not the same as tick `` ' ``.
- Blocks of code has three back-ticks around it ` ``` `.

```
s = "Hello World!"
print s
```

### Tables

```
Colons can be used to align columns.

| Tables        | Are           | Cool   |
| ------------- |:-------------:|:-------|
| col 3 is      | right-aligned | \$1600 |
| col 2 is      | centered      |   \$12 |

There must be at least 3 dashes separating each header cell. The outer pipes (|) are optional.
```

| Tables   |      Are      | Cool   |
| -------- | :-----------: | :----- |
| col 3 is | right-aligned | \$1600 |
| col 2 is |   centered    | \$12   |

### Quotes

Quote text with greater sign `>`.

> All that glitters is not gold
> Fair is foul, and foul is fair: Hover through the fog and filthy air.
> **These violent delights have violent ends...**

### Lists

- itemize
- with `-`

or

1. enumerate
2. with `1.`

### $\LaTeX$ support

- To write inline $\LaTeX$ formula, use `$` to surround `$\LaTeX$` syntax.
- To write math display, use `$$` to surround it.
  $$y_i = a x_i + b + \varepsilon.$$

### Hyper-link

- Use syntax `[text](link)` for links
- Use syntax `![text](link)` for figures

### Horizontal line

Draw a horizontal line with `***` or `___`

***

# Code cells

Code cells allow you to write Python codes and run them.

## Code style

**Programming style**, also known as **code style**, is a set of rules or guidelines used when writing the source code for a computer program. Following a particular programming style will help programmers _read and understand source code_ conforming to the style, and help to avoid introducing errors.

**The grading of your project will take coding style into account.  Please keep your code clean and readable.**

## 1. Comments

---

- Comments do not change the outcome of a program
- Comments are the way to improve the readability of a code
- Comments are **REQUIRED** in your assignments and projects. If there are no comments to explain your code, wrong output will get **ZERO POINT**.

A **inline comment** starts with `#`.


```python
# This is a comment. It explains your code in the following line(s).
print('Hello world!') # Comments can be added after the code.
```

    Hello world!


A **block comment** is surrounded by `"""`


```python
"""
Documentation string helps the user to understand the 
input/output/functionality of the module/function you wrote.
"""
def sample_average(data):
    """Return the sample average.
    
    Arguments:
    data -- a python list of real numbers
    """
    return sum(data)/len(data)
```


```python
x = [1,2,3]
sample_average(x) # call the funciton we defined just now
```




    2.0



### **PLEASE AVOID**  excessively long lines:


```python
# looooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooog
```

### String quotes

- Both single quote `'` and double quote `"` are allowed.
- However, please pick a rule and stick with it.
- **Raw string**: use `r""` to treat the special characters as literal character.
- When a string contains single or double quote characters, use the other one to surround the string.


```python
my_raw_string = r"/User\n/Downloads" # raw string treat \n as literal characters
print(my_raw_string)
```

    /User\n/Downloads



```python
my_string = "/User\n/Down\tloads" # string treat \n as new line and \t as tab
print(my_string)
```

    /User
    /Down	loads



```python
my_greatings = '"Hey!"'  # to use double quote in the string
print(my_greatings)
```

    "Hey!"


## 2. Variable names

Appropriate variable name helps the user to **understand its meaning**.

Usual naming styles:

- **Recommended:** `lower_case_with_underscores`: Function names should be lowercase, with words separated by underscores as necessary to improve readability. Variable names follow the same convention as function names.
- `b`
- `B` Case sensitive: `num` and `NUM` are two different variables in python.
- `lowercase`
- `UPPERCASE`: Module level constant usually use upper case.
- `UPPER_CASE_WITH_UNDERSCORE`: Module level constant usually use upper case.
- `CapitalizedWords`: case name is usually caped words.
- Bad examples: `x1`, `x2`, `x_123`.
- Good examples: `total_population`, `income_var`.

**Important rules:**

1. Start with either a letter or an underscore `_`: `_strs`, `strs`, `num`, `_num`
2. Cannot start with a number. For example: `9num` is not a valid variable name.
3. Cannot have special characters such as `` % ``, `` $ ``,  `` # `` etc. Invalid:  `` w#4  ``,  `` 0-9  ``.
4. Case sensitive: `num` and `NUM` are two different variables in python.
5. Special keywords cannot be used as variables, e.g., `def`, `int`, `type`, `etc`


## 3. Indentation

Indentation is of utmost importance in Python. Python interpreter use indentation to help interpret your code.
Wrong indentation will result in error.

- Use 4 spaces or one `tab` per indentation level.
- Python 3 **disallows** mixing the use of tabs and spaces for indentation.
- Continuation of codes should lie in the same indentation level.
- Clean indentation help the reader to understand your logic.


```python
x, y = 1, 2
 print( x == y ) # wrong indentation, extra blank space inserted
```


      File "<ipython-input-8-a343596f3244>", line 2
        print( x == y ) # wrong indentation, extra blank space inserted
        ^
    IndentationError: unexpected indent



- Each flow control (`if...elif`, `while`, and `for`) introduce a new level of indentation


```python
numbers = [1, 2, 4, 6, 11, 20]

# iterating over the given list
for val in numbers:   # no indentation here
    print(val)        # indentation here
```

- **hanging indent** (continuation lines): there should be no arguments on the first line and further indentation should be used to clearly distinguish itself as a continuation line.


```python
def long_function_name(
        var_one, var_two, var_three, # Add 4 spaces (an extra level of indentation) 
        var_four):                   # to distinguish arguments from the rest.
    print(var_one)

var_one, var_two, var_three, var_four = 1, 2, 3, 4

# BAD EXAMPLE
def long_function_name(
    var_one, var_two, var_three,  # Further indentation required as indentation is not distinguishable.
    var_four):
    print(var_one)


# GOOD EXAMPLE
foo = long_function_name(var_one, var_two,    # it is okay to break on line into continuation lines
                         var_three, var_four) # in which case new lines should be aligned

# BAD EXAMPLE
# Arguments on first line forbidden when not using vertical alignment.
foo = long_function_name(var_one, var_two,
    var_three, var_four)                      # new line is not aligned

# GOOD EXAMPLE
my_list = [   # The closing brace/bracket/parenthesis on multiline constructs may either line up 
    1, 2, 3,  # under the first non-whitespace character of the last line of list
    4, 5, 6,
    ]
```

# Requirements for the homework

---

1. All libraries should be imported upfront.
2. Homework is submitted in the format: 'Stats_HW2_ID_Name.ipynb'
3. The file is titled in the format: 'Stats_HW2_ID_Name'
4. Comments are **REQUIRED** in your assignments and projects. If there are no comments to explain your code, wrong output will get **ZERO POINT**.
5. **Before submission**: click on the `Kernel` $\to$ `Restart & Run All`. Make sure that there is NO error.
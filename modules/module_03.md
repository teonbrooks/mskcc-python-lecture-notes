---
# title: Module 3: Built-in Functions, Control Flow, Numpy
marp: true
theme: gaia
footer: Intro to Scientific Python
authors: Teon Brooks
---
<style>
    footer {
    text-align: right;
    }
</style>

# Module 3: Built-in Functions and Control Flow

October 6, 2025

---
<style scoped>section { font-size: 28px; }</style>
Content covered:

## H1

1. Built-in Functions and libraries
2. Control Flow (If/Else)

## H2

1. For loops
2. Functions

---

## Some common Built-in Functions in Python

---

### Numerics

- abs()
- max()
- min()

---

### Boolean

- any()
- all()
- bool()

---

- len()
- input()
- range()

---

### Type-related functions

- dict()
- float()
- int()
- list()
- str()
- set()
- tuple()

---

## All the Built-in Functions in Python

https://docs.python.org/3/library/functions.html

---

## 🐍 Python trick

You can get any information about a variable, built-in type, function, etc. by adding a question mark after it.

```python
print?
```

---

## Exercise

Spend some time exploring the different built-in functions in Python.

Q: How is `all()` different from `any()`?

Q: What happens when you give a string to a list function?

Q: What happens if you give a string to an int?

---

## Python Standard Library

https://docs.python.org/3/library/index.html

---

## Truthiness

This operates on understanding the boolean value of an object. In Python, here are some of the default boolean values when evaluating objects:

Constants defined to be false:

- None and False
- zero of any numeric type: 0, 0.0, 0j, Decimal(0), Fraction(0, 1)
- empty sequences and collections: '', (), [], {}, set(), range(0)

---

## Boolean Operators

| Operation | Meaning |
| --------- | ------- |
| < | strictly less than |
| <= | less than or equal |
| > | strictly greater than |
| >= | greater than or equal |
| == | equal |
| != | not equal |

---

## Boolean Operators, cont.

When evaluating objects:

| Operation | Meaning |
| --------- | ------- |
| is | object identity |
| is not | negated object identity |

---

## Control Flow

These are statements used to connect your script together either through some decision (e.g. if/else) or through iteration (e.g. for loops).

---

## If/Else

Python uses an If-Elif-Else paradigm for conditional execution.

Instead of paranthesis and curly brackets to demarcation, Python uses spaces. 

In modern text editors, you can use tab to define scope. Most editors will convert tabs into four spaces.

---

Let's break this down:

```python
if 5 > 6:
    print("the universe is broken")
elif len("cat") > len("dog"):
    print("uh oh, something is wrong in the world")
else:
    print("math is still mathing")
```

`if` condition is true:
    do this thing
`elif` (contraction of else if) is evaluated only if the first condition is not met
Else will be executed if neither the `if` or `elif` is satisfied.

---

## Exercise

Let's now jump to our editor for this portion.

- Create a dictionary.
- Write a few different if-elif-else statements
  - Check whether a key is in the dictionary
    - If a key does not exist, add an entry to the dictionary
  - If a key does exist, check if it is a list
    - If it's not a list, convert it to a list
    - If it's a list append a value to its list

---

## For Loops

We've talked about iterables but what exactly does that mean?

Iterables are objects you can iterate over.

```python
numbers = [1, 2, 3, 4, 5]
```

---

In Python, we can iterate of lists, dictionaries, etc. when we want to perform an operation.

We use the keyword `for` when we want to iterate over a list.

```python
for number in numbers:
    print(number)
```

Python has a neat feature that when it iterates over the list, it actually returns a copy of value from the thing you're iterating over.

---
This is useful if you want to create a new object based on another one.

```python
numbers_squared = list()
for number in numbers:
    numbers_squared.append(number ** 2)
```

---

You can also pair your for-loop iterations with the `enumerate` function.

`enumerate` will return an incremented count on your iterable, starting with zero by default, zipped to your iterable. The returned value is a tuple of the incrementer and your iterable. `start` is an argument.

```python
for value in enumerate(numbers):
    value
```

```python
for index, number in enumerate(numbers):
    print(f"Index is: {index}")
    print(f"Number is: {number}")
```

---

## Functions

Functions are useful when you have a block of code that you would like to reuse elsewhere.

Functions in Python are defined using the def keyword.
They are often written in lowercase and uses snake case, e.g. `python_func()`.

```python
def print_hello_world():
    print("Hello world!")
```

---

## Functions, cont.

Sometimes you want your function to take in an input and manipulate it:

- Introducing f-strings

```python
def print_hello_person(person):
    print(f"Hello {person}!")
```

---
## Functions, cont.

Maybe you don't want to just print things to your console, but you want to be able to store the output value

- Introducing f-strings

```python
def print_hello_person(person):
    return f"Hello {person}!"
```

```python
new_string = print_hello_person("Teon")
new_string
```

---

## Exercise

1. Create a function that takes in a list and returns a dictionary where the keys are indexes.

2. Create a function that takes a list, it creates a list in reverse, and returns a list of tuples of both lists combined.

3. Create a function that that prints three different messages based on the input type.

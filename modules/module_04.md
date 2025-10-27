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

# Module 4: Intro to Numpy

October 8, 2025

---
<style scoped>section { font-size: 28px; }</style>
Content covered:

## H1

1. Intro to Numpy
   1. NDarray
   2. Numeric operations
2. Brainstorming First Assignment

---

## H2: Numpy

---

## Numpy

Numpy is one of the core scientific libraries in Python. It has its own data type, the `numpy.ndarray`, which is an n-dimensional array. This is not a built-in library although it is one of the most common libraries used.

These arrays are used primarily to store numerical data of the same type, and has a host of methods and functions to perform numerical analysis and computation.

---

## Getting Started

```python
import numpy as np
```

In Python you can alias an import using the `as` keyword. A common practice is to refer to `numpy` as `np`.

---

```python
arr = np.array([1, 2, 3, 4])
```

`arr` has some important methods:
- `ndim`: number of dimensions
- `shape`: the dimensions of the array
- `dtype`: the data type of the array

`np.array` takes an object as an argument e.g. list, tuple, but not individual values.

---

## Some common arrays you can use

`np.zeros()` takes an int or list/tuple of ints as its argument and returns an array of zeros with those dimensions.

`np.ones()` is the same as above but returns ones.

`np.arange()` similar to built-in `range`, but returns an array.

`np.linspace()` takes a start, stop, and number of steps, and returns an array with evenly spaced value in the range.

---

## Exercises

Try out some of these common array functions in your iPython session.

---

# Random Numbers

rng = np.random.default_rng()
rng.random()

---

## Array manipulation

`.reshape()` this method is used to change the shape of an array. This methods accepts the resulting dimensions as separate arguments or they can be a list/tuple.

```python
arr = np.arange(24)
arr.reshape(4,6)
arr.reshape(2,4,3)
```

`.ravel()` flattens the dimensionality into a 1-d array.

---

`.sum()` will return the sum of the entire array.

If you want to return the sum across the rows or across the columns, you can use the `axis` parameter.

`axis=0`, refers to column-wise operation where the summation will be done along the column.

`axis=1` would refer to a row-wise operation.

The same goes for `.min()`, `.max()`, `.cumsum()`, etc.

---

## Let's try some of the methods together.

---

By default, multiplying array is element-wise. It uses the `*` operator.

For matrix multiplication, use the `@` operator.

If you need to perform a scalar operation over an array, this is often referred to as broadcasting. It will perform element-wise multiplication of the scalar on the array.

Broadcasting can also be done between two arrays if the trailing dimensions are equivalent.
<!-- https://numpy.org/doc/stable/user/basics.broadcasting.html -->

```python
arr = np.arange(24).reshape([8,3])
scaler = np.array([1,2,3])
new_arr = arr * scaler
```

---

## Combining arrays

`np.hstack()`: this will horizontally stack values along the first dimension, column-wise.

`np.vstack()`: this will vertically stack values, row-wise.

---

## Exercises

1. Create a function that takes in a list, a parameter for vertical or horizontal or None, returns array with a duplication either horizontally, vertically, or none at all.

---

## <!-- fit -->Brainstorming First Assignment

1. What is a topic you would like to do some data analysis on?
2. Find a dataset related to this topic.
3. What are the types of analyses you would like to conduct?
4. What are some of the plots you would like to see?

Project will be due on October 20.
We will go over this in more detail in our next class, October 15.

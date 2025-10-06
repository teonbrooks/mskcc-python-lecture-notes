---
# title: Module 2: Control Flow, Functions, and Classes
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

# Module 2: Project Organization and Common Data Types

October 1, 2025

---

Content covered:

## H1

1. Tools
2. Project Organization

## H2

1. Common Data Types

---

## H1

Refer to Module 1

---

## H2

1. Common Data Types

---

## Strings

Strings are data objects in Python that can store characters.

In general objects can have functions stored in them called methods. We will go into more detail about this later in the course.

To access the methods of an object, add a period following the object's name and hit tab.

You can use a pair of single quotes `''` or a pair of double quote `""` to denote a string. If you would like to include a single quote in your string then use a double quote, and vice versa.

---

## Strings, cont.

Here are some common methods you might use with a string:

- `join`: this will allow you to combine strings together
- `split`: this will allow you to divide a string into a list
- `upper`: it converts a string to all uppercase
- `lower`: it converts a string to all lowercase

---

## Exercise

Let's try some of these methods in our iPython session.

- Assign a string to a variable.
- Check out all the methods available to it by using tab completion.
- Try to use at least three different methods

---

## Lists

Lists are containers. They can hold other data types within them. They are also iterables, which means you can iterate over them.

Here are some common methods:

- `append`: this adds an object to the given list
- `extend`: this combines another list or iterable
- `index`: returns the index of a value

---

## Lists, cont.

You can index particular elements in a list. Python is a zero-based indexing language, which means the first item in a list will be index 0.

```python
numbers = [1,2,3,4,5]

numbers[0]
1
```
Index of `-1` has a special meaning. It will index the last element in a list.

---

Lists, cont.

You can also index a subset of values in a list. This is called a slice. This time, the result will be a list.

```python
numbers[2:4]
[3, 4]
```

If you want to return every second of a list, you can use the following notion:

```python
numbers[::2]
[1, 3, 5]
```

---

## Lists, cont.

The general case for the slice is listed below:

```python
list[start:stop:step]
```

---

## Strings, revisited

Now that we know how to create lists, let's go out the following two string methods:

- `.join`
  
  Takes a list or other iterable as its argument and concatenates with the given string.

```python
'-'.join(['apples', 'oranges', 'strawberries'])
'apples-oranges-strawberries'

fruit_string = _
```

---

## Strings, revisited cont.

- `.split`

  Splits a string based on a string into a list.

```python
fruits = fruit_string.split('-')
```

---

## Dictionaries

Dictionaries are also a type of container. They are a mapping type where its content is stored in pairs of keys and values, also known as entries.

```python
my_dict = {'pet': 'cat',
           'animals': ['cats', 'dogs', 'birds']
          }
```

You can also use the `dict()` constructor to create a dictionary. However, keys cannot contain symbols such as `-`, `*`.

---

## Dictionaries, cont.

You can retrieve the content of a dictionary by using the key as the index.

```python
my_dict['pet']
'cat'
```

You can also use the `.get` method to retrieve a value from a dictionary. This method also has a default argument for when the key isn't in the dictionary.

Question: what happens when you use key indexing method when the key isn't in the dictionary?

---

## Exercise

Let's create a dictionary with different data types as values,
e.g. string, list, dict, etc.

- Try to add a new append a list to one of those values in your dictionary.
- Try to extend a list to one of those values in your dictionary.
- Try to add a new entry to one of those values in your dictionary.

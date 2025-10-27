---
# title: Classes and Intro to Jupyter
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

# Module 5: Classes and Intro to Jupyter

October 15, 2025

---
<style scoped>section { font-size: 28px; }</style>
Content covered:

## H1

1. Classes
2. Jupyter Notebooks
3. Intro to Matplotlib
   1. Pyplot
<!-- 3. Brainstorming First Assignment -->

---

## Classes

Classes, also called Objects, are containers in Python that can store values, known as `attributes`; and functions, known as `methods`

---

## Anatomy of a Class

Classes are defined using `class` keyword:

```python

class MyClass:
    def __init__(self, attribute1):

        self.attribute1 = attribute1

```

---

## Classes cont.

You can also include functions that will be stored in the object by default too:

```python

class MyClass:
    def __init__(self, attribute1):

        self.attribute1 = attribute1

    def stringify(self, value):

        return str(value)

```

---

## Jupyter Notebooks

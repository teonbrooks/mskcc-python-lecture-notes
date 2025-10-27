---
# title: Module 8: Review cont., Pandas cont., Seaborn
marp: true
theme: gaia
footer: Intro to Scientific Python
authors: Teon Brooks
---
<style>
    footer {
    text-align: right;
    }

    pre, code {
        background-color: ghostwhite !important;
        color: black;
}
</style>

# Module 8: Review cont., Pandas cont., Seaborn

October 22, 2025

---

## Review

---

## Things We've Covered, cont.:

- Numpy
  - ndarray
  - random number generator 
- Matplotlib
  - pyplot
  - fig, ax = plt.subplots()

---

## Things We've Covered, cont.:

- Pandas
  - Dataframes
  - Series
  - Groupby

---

## Pandas, cont.

Pandas has two main datatypes: Series and Dataframes

Dataframes are the containers of Series.

Series a collection of values that all have the same datatype.

---

## Loading Data using Pandas

```python
import pandas as pd

df = pd.read_csv('../module_07/gapminder.tsv', sep='\t')
```

Notice that you can import files using relative paths.

```bash
(base) ➜  mskcc-python tree ~/workspace/mskcc-python 
/Users/teonbrooks/workspace/mskcc-python
├── module_07
│   ├── gapminder.tsv
│   └── module_07.ipynb
└── module_08
    └── module_08.ipynb
```

---

## Indexing with Boolean expressions

Pandas lets you do truth evaluation for a Series in your dataframe by writing Boolean expressions.

```python
df['continent'] == 'Africa'
```

This returns a series that consists of `True` and `False` for the values in a given series.

---

## Indexing, cont.

We can use Boolean expressions to select a subset of data from our dataframe

```python
df[df['continent'] == 'Africa']
```

What this expression does is look at the column `df['continent']` and see if the value in the column is equal `Africa`.

It only returns the rows where the Boolean expression is true.

---

## Indexing, cont.

Pandas also has a convenient method for its dataframes to write these queries.

```python
df.query("continent == 'Africa'")
```

Notice that you need to provide a string to the query method. In this example, we are evaluating against a string therefore we need different string literals within our expression.

---

## Renaming Columns

- .rename()

```python
.rename(columns = {"old_name": "new_name"})
```

---

## Renaming Columns, cont.

```python
df.rename(
    columns = {
        'lifeExp': 'life_expectancy'
})
```

To prevent overwriting your dataframe, Pandas creates a copy of your dataframe.

If you want to modify your existing dataframe, you would need to use the argument `inplace` and set it `inplace=True`.

<!-- ---
## Creating New Columns

- create a new column with apply -->
---

## Exercise

Let's do some more exploration of the Gapminder dataset.

- Create a breakdown by year and country of the average life expectancy and the average GDP per capita
- Create another breakdown by year and continent
- Create a breakdown by year for average life expectancy and GDP per capita
- Create a figure with two subplots with the two calculated averages

---

## Cheatsheet

https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf

---

<!-- ## Groupby with Plots

```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()

groups = dict()
for labels, group in df.groupby(['continent', 'year']):
    continent, year = labels
    lifeExp = group.mean()
    groups[continent]
``` -->

## Plotting with Seaborn

We will be using `seaborn` as a plotting library with our dataframes.

Seaborn is a high-level visualization library that works on top of matplotlib.

It gives some very nice features to make plotting data in dataframes easy.

---

## Seaborn

First, we will need to install Seaborn.

In your terminal, you can install seaborn using `pip`.

```bash
pip install seaborn
```

---

## Seaborn, cont.

By convention, we import seaborn as `sns`.

```python
import seaborn as sns
```

TIL: `sns` comes from an inside joke about West Wing and the character, Samuel Norman Seaborn.

ref: https://github.com/mwaskom/seaborn/issues/229

---

Seaborn lets us convenient make plots and we can pass matplotlib `Axis` to target the location of the plots.

```python
import matplotlib.pyplot as plt
import seaborn as sns


fig, ax = plt.subplots(1, 2)
sns.lineplot(x='year', y='lifeExp', data=df, ax=ax[0], linestyle=':')
sns.lineplot(x='year', y='lifeExp', data=df, ax=ax[1], linestyle='-.')
```

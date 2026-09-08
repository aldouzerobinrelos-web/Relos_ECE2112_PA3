# Relos_ECE2112_PA3

The content of this repository contains Programming Assignment 3 for the course "Advance Computer Programming" S.Y. 2026 - 2027. This project covers 3 python problems connected to Module 3 - Python Data Analysis (Pandas)

# A. POSITIONAL AND LABEL-BASED SLICING

After loading `cars`, complete the following operations.

a. Display the shape and complete list of column names of `cars`.

b. Using positional slicing, create `cars_6_to_10` containing rows 6 through 10 of the dataset, where the first data row is row 1.

c. From `cars_6_to_10`, display only the columns `Model`, `mpg`, `cyl`, `hp`, and `gear`, in that order.

---

```python
cars = pd.read_csv('cars.csv')
cars.loc[0:100, ['Model']]
```

`cars = pd.read_csv('cars.csv')` loads the `cars.csv` file into the DataFrame `cars`. `cars.loc[0:100, ['Model']]` uses label-based slicing to display the `Model` column for the available rows in the dataset.

```python
display(cars.loc[0:100, ['Model']].shape)
```

This displays the shape of the selected `Model` column. The output `(32, 1)` means that the selection contains 32 rows and 1 column.

```python
cars_6_to_10 = cars.iloc[5:10, [0, 1, 2, 4, 10]]
```

`cars.iloc[5:10, [0, 1, 2, 4, 10]]` uses positional slicing to select rows 6 through 10 and the columns at positions 0, 1, 2, 4, and 10. These correspond to `Model`, `mpg`, `cyl`, `hp`, and `gear`.

```python
display(cars_6_to_10)
```

This displays `cars_6_to_10` containing rows 6 through 10 with only the `Model`, `mpg`, `cyl`, `hp`, and `gear` columns.

# B. MODEL LOOKUP

Use Boolean indexing on the `Model` column to answer both requests.

a. Display the complete row for Toyota Corolla.

b. For Pontiac Firebird, display only `Model`, `mpg`, `hp`, and `wt`.

Store the two results in `Toyota_Corolla` and `Pontiac_Firebird`, respectively. Do not use a hard-coded row number to locate either model.

---

```python
Toyota_Corolla = cars.loc[cars['Model'] == 'Toyota Corolla']
Pontiac_Firebird = cars.loc[(cars['Model'] == 'Pontiac Firebird'),['Model', 'mpg', 'hp', 'wt']]
```

`cars['Model'] == 'Toyota Corolla'` uses Boolean indexing to locate the `Toyota Corolla` row without using its row number. The complete row is stored in `Toyota_Corolla`.

`cars['Model'] == 'Pontiac Firebird'` uses Boolean indexing to locate the `Pontiac Firebird` row. The column list limits the result to `Model`, `mpg`, `hp`, and `wt`, which is stored in `Pontiac_Firebird`.

```python
display(Toyota_Corolla)
```

`display(Toyota_Corolla)` displays the complete row containing all the information for the Toyota Corolla.

```python
display(Pontiac_Firebird)
```

`display(Pontiac_Firebird)` displays the Pontiac Firebird with only the `Model`, `mpg`, `hp`, and `wt` columns.

# C. MULTI-MODEL SUBSETTING

---

Thank you for reading!

For the main program for Programming Assignment 3 click this link

https://github.com/aldouzerobinrelos-web/Relos_ECE2112_PA3/blob/main/Relos_ECE2112_PA3.ipynb

then download, then open on Google Colab or Jupyter Notebook, and run every cell.

**Readme File History:**

September 7 2026 - Initial Readme file upload

September 8 2026 - Started and finished the 1st and 2nd problem


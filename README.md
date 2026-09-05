# ELVAMBUENA_2ECE-D_PA3
Made by: Samantha B. Elvambuena | 2ECE-D

This contains the Programming Assignment 3 for our course "Advance Computer Programming" this A.Y. 2026-2027. This project covers three python problems relevant to the Module 3 - Python Data Analysis (PANDAS).
## Objectives of the Experiment
>At the end of this laboratory activity, the student should be able to:
>1. load a CSV dataset into a Pandas DataFrame;
>2. select rows and columns using positional and label-based indexing;
>3. filter records using conditions on a DataFrame column; and
>4. extract a well-defined subset of data without changing the source data.
## A. POSITIONAL AND LABEL-BASED SLICING
>After loading cars, complete the following operations.
>a. Display the shape and complete list of column names of cars.
>b. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where the first data row is row 1.
>c. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.
The following functions were used in this problem:
Firstly, PANDAS should be initialized by:
```python
import pandas as pd
```

```python
cars=pd.read_csv('cars.csv')
cars
```

```python
print('Shape:',cars.shape)
print(cars.loc[:,['Model']])
# output
Shape: (32, 12)

```

```python
cars_6_to_10=cars.iloc[5:10]
cars_6_to_10
```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```

```python

```


```python

```

```python

```

```python

```

```python

```

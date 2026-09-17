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
First, to read and write CSV file as there is a provided **cars.csv file** which contains the needed information **pd.read_csv()** is used.
```python
cars=pd.read_csv('cars.csv')
cars
```
The built-in function **.shape** is used to display the shape of the car and **.columns** for the complete list of column names of cars.
```python
print('Shape:',cars.shape)
print(cars.columns)
# output
Shape: (32, 12)
Index(['Model', 'mpg', 'cyl', 'disp', 'hp', 'drat', 'wt', 'qsec', 'vs', 'am',
       'gear', 'carb'],
      dtype='object')
```
Positional slicing **.iloc** is used to generate the cars 6 to 10 containing rows 6 through 10 of the dataset, as **5** the first integer that is inclusive and **10** is the last integer that is exclusive. And the data is stored in **cars_6_10**.
```python
cars_6_to_10=cars.iloc[5:10]
cars_6_to_10
```
Then, to locate the specific columns (Model, mpg, cyl, hp, and gear, in that order) from cars 6 to 10 the function **.loc** is used to select single row of subset of rows. The operator ":" is used to generate the whole section as there is no indicated index.
```python
cars_6_to_10.loc[:,['Model', 'mpg', 'cyl', 'hp',  'gear']]
# output
	Model	      mpg	  cyl	 hp 	gear
5	Valiant    	18.1	6	   105	3
6	Duster 360  14.3	8	   245	3
7	Merc 240D	  24.4	4	   62 	4
8	Merc 230	  22.8	4	   95 	4
9	Merc 280 	  19.2	6	   123	4
```
## B. MODEL LOOKUP
>Use Boolean indexing on the Model column to answer both requests.
>a. Display the complete row for Toyota Corolla.
>b. For Pontiac Firebird, display only Model, mpg, hp, and wt.
>Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to locate either model.

The following functions were used in this problem:
>Since PANDAS is already initialized in the first problem we can move on to the next function.

To display the complete row for Toyota Corolla boolean indexing is used to generate only the row for Toyota Corolla.
```python
cars[cars['Model']=='Toyota Corolla']
# output
             Model  mpg	  cyl	disp	hp	drat	wt	  qsec	vs	am	gear	carb
19	Toyota Corolla	33.9	4	  71.1	65	4.22	1.835	19.9	1	  1	  4	    1
```
To display the row for Pontiac Firebird boolean indexing is used and **.loc** is used to indicate the specific columns needed by providing the specific index (Model, mpg, hp, wt).
```python
cars.loc[(cars['Model']=='Pontiac Firebird'), ['Model', 'mpg', 'hp', 'wt']]
# output
               Model	mpg	  hp	wt
24	Pontiac Firebird	19.2	175	3.845
```
## C. MULTI-MODEL SUBSETTING
>Create a DataFrame named selected cars containing only the records for three models: Datsun 710, Lotus Europa, and Ferrari Dino.
>For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values rather than by row numbers. Display selected cars and its shape.
```python
selected_cars=pd.DataFrame(cars.loc[(cars['Model']=='Datsun 710')| (cars['Model']=='Lotus Europa')| (cars['Model']=='Ferrari Dino'), ['Model', 'mpg', 'cyl', 'hp', 'gear']])
selected_cars
# output
           Model	mpg	cyl	hp	gear
2	  Datsun 710	  22.8	4	93	4
27	Lotus Europa	30.4	4	113	5
29	Ferrari Dino	19.7	6	175	5
```
The built-in function **.shape** is used to display the shape of the selected_car and **.loc** to generate the Model section of the selected cars.
```python
print(selected_cars.loc[:,['Model']])
print('Shape:', selected_cars.shape)
# output
           Model
2     Datsun 710
27  Lotus Europa
29  Ferrari Dino
Shape: (3, 5)
```

Thank you for reading!

To see the main python program, click this [link](https://github.com/samanthaelvambuena-rgb/ELVAMBUENA_2ECE-D_PA3/blob/main/PA3_ELVAMBUENA.ipynb) and download.

### HISTORY
September 17, 2026 - Made a minor correction to README.

September 6, 2026 - Final touches made the final improvements and corrections to the code and README.

September 3, 2026 - README structure Created the overall structure and organization of the README.

September 3, 2026 - Initial commit Created the initial code and implemented the main functionality of the project.

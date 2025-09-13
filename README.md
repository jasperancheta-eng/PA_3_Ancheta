# 📘 PA 3 – Programming Assignment  

👨‍💻 Author: Jasper Ancheta <br>
📅 Date: September 14, 2025 <br>
📚 Course: ECE2112 – Programming Assignment

---

# 📌 Version History  

- **V1.0 (09-14-24)** – Initial Release and Submission of GitHub Link  
- **V1.1 (09-14-24)** – Added README Documentation for Problems  

---

# 📌 Problem 1: Pandas DataFrame Loading  

This problem loads the **Cars dataset** into a Pandas DataFrame named `cars` and displays the first and last five rows.  

### Steps:  
1. Import pandas as pd.
2. Load cars.csv into a DataFrame cars.
3. Display the first 5 rows using .head().
4. Display the last 5 rows using .tail().

---

## ✅ Input:  
```python
# PA 3 – Problem 1: Load Cars Dataset

import pandas as pd

# Load dataset
df = pd.read_csv("cars.csv")

# Show first 5 rows
print("First five rows:")
cars.head()

# Show last 5 rows
print("Last five rows:")
cars.tail()
```
## ✅ Output:  
```
First five rows:
         Model   mpg  cyl  disp   hp  drat     wt   qsec  vs  am  gear  carb
0     Mazda RX4  21.0    6   160  110  3.90  2.620  16.46   0   1     4     4
1 Mazda RX4 Wag  21.0    6   160  110  3.90  2.875  17.02   0   1     4     4
2    Datsun 710  22.8    4   108   93  3.85  2.320  18.61   1   1     4     1
3 Hornet 4 Drive 21.4    6   258  110  3.08  3.215  19.44   1   0     3     1
4 Hornet Sportabout 18.7 8   360  175  3.15  3.440  17.02   0   0     3     2

Last five rows:
          Model   mpg  cyl  disp   hp  drat     wt   qsec  vs  am  gear  carb
27  Lotus Europa  30.4    4   95.1 113  3.77  1.513  16.9   1   1     5     2
28 Ford Pantera L 15.8    8  351.0 264  4.22  3.170  14.5   0   1     5     4
29   Ferrari Dino 19.7    6  145.0 175  3.62  2.770  15.5   0   1     5     6
30 Maserati Bora  15.0    8  301.0 335  3.54  3.570  14.6   0   1     5     8
31    Volvo 142E  21.4    4  121.0 109  4.11  2.780  18.6   1   1     4     2
```

# 📌 Problem 2: Subsetting, Slicing, and Indexing

This problem uses the same DataFrame cars from Problem 1 and extracts specific data using subsetting, slicing, and indexing.

Steps:

a. Display the first five rows with odd-numbered columns (1, 3, 5, 7...).
b. Display the row that contains the model Mazda RX4.
c. Find how many cylinders (cyl) the model Camaro Z28 has.
d. Show the cylinders and gear type of Mazda RX4 Wag, Ford Pantera L, and Honda Civic.

---

## ✅ Input:
```
# PA 3 – Problem 2: Subsetting, Slicing, Indexing

# a. First 5 rows, odd columns only
print("First five rows with odd-numbered columns:")
cars.iloc[:5, ::2]

# b. Show row for Mazda RX4
print("Row for Mazda RX4:")
cars[cars["Model"] == "Mazda RX4"]

# c. Show cylinder value of Camaro Z28
print(cars[cars['Model'] == 'Camaro Z28']['cyl'].values[0])

# d. Show cylinder and gear for Mazda RX4 Wag, Ford Pantera L, and Honda Civic
print("Cylinders and gear type for Mazda RX4 Wag, Ford Pantera L, and Honda Civic:")
cars.loc[cars["Model"].isin(["Mazda RX4 Wag", "Ford Pantera L", "Honda Civic"]), ["Model", "cyl", "gear"]]
```

## ✅ Output:
```
First five rows with odd-numbered columns:
     Model  cyl   hp     wt  vs  gear
0   Mazda RX4    6  110  2.620   0     4
1 Mazda RX4 Wag  6  110  2.875   0     4
2  Datsun 710    4   93  2.320   1     4
3 Hornet 4 Drive 6  110  3.215   1     3
4 Hornet Sportabout 8 175  3.440  0     3

Row for Mazda RX4:
      Model   mpg  cyl  disp   hp  drat    wt   qsec  vs  am  gear  carb
0  Mazda RX4  21.0    6   160  110   3.9  2.62  16.46   0   1     4     4

Number of cylinders in Camaro Z28:
8

Cylinders and gear type for Mazda RX4 Wag, Ford Pantera L, and Honda Civic:
            Model  cyl  gear
1    Mazda RX4 Wag    6     4
18     Honda Civic    4     4
28  Ford Pantera L    8     5
```
# 🛠 Software(s) Used
<p align="left"> <img src="https://www.python.org/static/community_logos/python-logo.png" alt="Python Logo" width="120"/> <img src="https://jupyter.org/assets/homepage/main-logo.svg" alt="Jupyter Logo" width="90"/> </p>
📂 Repository Information

# Languages Used:

Python (100%)

# 🌦️ Weather Condition Data Analysis using Python & Pandas

## 📌 Project Overview

This is a **beginner-friendly Data Analysis project** using **Python, Pandas, and Jupyter Notebook**.

The project analyzes weather data and demonstrates how to perform basic data exploration, filtering, statistical analysis, and grouping using Pandas.

This project is mainly used for beginners who are learning **Python Data Analysis and Pandas**.

---

## 🎯 Project Objectives

The main objectives of this project are:

* Learn how to load a CSV dataset using Pandas
* Understand Pandas DataFrames
* Explore rows and columns
* Check data types
* Find unique values
* Count values
* Detect missing values
* Remove missing values
* Rename columns
* Calculate mean, standard deviation, and variance
* Filter records based on conditions
* Use `groupby()`
* Perform basic statistical analysis
* Practice real-world data analysis questions

---

## 🛠️ Technologies Used

| Technology       | Purpose                        |
| ---------------- | ------------------------------ |
| Python           | Programming language           |
| Pandas           | Data manipulation and analysis |
| NumPy            | Numerical operations           |
| Jupyter Notebook | Development environment        |
| CSV              | Dataset format                 |

---

## 📂 Project Structure

```text
Weather-Condition-Data-Analysis/
│
├── WeatherCondition.ipynb
├── Weather Data.csv
└── README.md
```

---

## 📊 Dataset

The project uses a **Weather Data CSV dataset** containing weather-related information.

Important columns used in the analysis include:

* Wind Speed
* Visibility
* Pressure
* Relative Humidity
* Weather Condition

---

## 🚀 Installation

### Step 1: Install Python

Download and install Python from the official Python website.

### Step 2: Install Required Libraries

Open Command Prompt or Anaconda Prompt and run:

```bash
pip install pandas numpy jupyter
```

### Step 3: Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
WeatherCondition.ipynb
```

---

# 🔍 Data Analysis Performed

## 1. Import Libraries

```python
import numpy as np
import pandas as pd
```

NumPy and Pandas are imported for numerical operations and data analysis.

---

## 2. Read the Dataset

```python
df = pd.read_csv("Weather Data.csv")
```

The CSV file is loaded into a Pandas DataFrame.

---

## 3. Explore the Dataset

### Display first five records

```python
df.head()
```

### Check number of rows and columns

```python
df.shape
```

### Generate statistical summary

```python
df.describe()
```

### Check DataFrame index

```python
df.index
```

### Display column names

```python
df.columns
```

### Check data types

```python
df.dtypes
```

### Check unique values

```python
df.nunique()
```

### Find unique weather conditions

```python
df['Weather'].unique()
```

### Count records

```python
df.count()
```

### Count each weather condition

```python
df['Weather'].value_counts()
```

### Get DataFrame information

```python
df.info()
```

---

# 🧹 Missing Value Analysis

The project also demonstrates how to identify and handle missing values.

### Find missing values

```python
df.isnull()
```

### Count missing values

```python
df.isnull().sum()
```

### Remove rows containing missing values

```python
df.dropna()
```

---

# 📝 Questions Solved in the Project

The notebook contains **15 practical Pandas questions**.

### Q1. Find all unique Wind Speed values

```python
df['Wind Speed_km/h'].unique()
```

---

### Q2. Find the number of times when Weather is exactly Clear

```python
df[df['Weather'] == 'Clear']
```

Also demonstrated using:

```python
df.groupby('Weather').get_group('Clear')
```

---

### Q3. Find the number of times when Wind Speed was exactly 4 km/h

```python
df[df['Wind Speed_km/h'] == 4]
```

---

### Q4. Find all Null Values

```python
df.isnull().sum()
```

---

### Q5. Rename Weather column

The column:

```text
Weather
```

is renamed to:

```text
Weather Condition
```

using:

```python
df.rename(
    columns={'Weather': 'Weather Condition'},
    inplace=True
)
```

---

### Q6. Find the Mean Visibility

```python
df.Visibility_km.mean()
```

---

### Q7. Find the Standard Deviation of Pressure

```python
df.Press_kPa.std()
```

---

### Q8. Find the Variance of Relative Humidity

```python
df['Rel Hum_%'].var()
```

---

### Q9. Find all instances when Snow was recorded

```python
df[df['Weather Condition'].str.contains('Snow')]
```

---

### Q10. Find records where:

* Wind Speed is above 24 km/h
* Visibility is 25 km

```python
df[
    (df['Wind Speed_km/h'] > 24) &
    (df['Visibility_km'] == 25)
]
```

---

### Q11. Find the mean value of each column for each Weather Condition

```python
df.groupby(
    'Weather Condition'
).mean(numeric_only=True)
```

---

### Q12. Find minimum and maximum values for each Weather Condition

Minimum:

```python
df.groupby('Weather Condition').min()
```

Maximum:

```python
df.groupby('Weather Condition').max()
```

---

### Q13. Show all records where Weather Condition is Fog

```python
df[df['Weather Condition'] == 'Fog']
```

---

### Q14. Find instances when:

* Weather Condition is Clear

**OR**

* Visibility is above 40 km

```python
df[
    (df['Weather Condition'] == 'Clear') |
    (df['Visibility_km'] > 40)
]
```

---

### Q15. Find instances when:

### Condition A

Weather is Clear **AND** Relative Humidity is greater than 50

### OR

### Condition B

Visibility is above 40

```python
df[
    (
        (df['Weather Condition'] == 'Clear') &
        (df['Rel Hum_%'] > 50)
    )
    |
    (df['Visibility_km'] > 40)
]
```

---

# 📚 Pandas Concepts Learned

This project covers the following important Pandas concepts:

```text
1. DataFrame
2. read_csv()
3. head()
4. shape
5. describe()
6. index
7. columns
8. dtypes
9. nunique()
10. unique()
11. count()
12. value_counts()
13. info()
14. isnull()
15. notnull()
16. dropna()
17. rename()
18. mean()
19. std()
20. var()
21. str.contains()
22. Filtering
23. AND condition (&)
24. OR condition (|)
25. groupby()
26. min()
27. max()
```

---

# 💡 What I Learned

Through this project, I learned how to:

* Work with CSV files
* Create and explore Pandas DataFrames
* Understand rows and columns
* Check data quality
* Handle missing values
* Filter data using conditions
* Perform statistical calculations
* Group data based on categories
* Analyze weather conditions
* Solve real-world data analysis questions using Python

---

# 👨‍💻 Suitable For

This project is suitable for:

* Python Beginners
* Pandas Beginners
* Data Analytics Beginners
* Students preparing for Data Analyst interviews
* Students learning Jupyter Notebook

---

# 🔮 Future Improvements

The project can be extended by adding:

* 📊 Matplotlib visualizations
* 📈 Seaborn charts
* 📉 Weather trend analysis
* 🌡️ Temperature analysis
* 💨 Wind-speed analysis
* 🌧️ Weather-condition distribution
* 📊 Interactive Power BI dashboard
* 🗄️ SQL-based analysis
* 🤖 Machine Learning weather prediction

---

# ⭐ Conclusion

This project provides a simple introduction to **Data Analysis using Python and Pandas**.

It focuses on understanding the basic operations required to explore, clean, filter, and analyze a real-world weather dataset.

It is a good starting project for beginners who want to build a foundation in **Python, Pandas, and Data Analytics**.

---

### Skills Demonstrated

```text
Python
Pandas
NumPy
Data Cleaning
Data Exploration
Data Analysis
Jupyter Notebook
```

---

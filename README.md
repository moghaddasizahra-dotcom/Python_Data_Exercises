# Python Data Exercises

This repository contains Python exercises covering **FizzBuzz** and **Data Analysis using Pandas**.  
The exercises include tasks such as loading and exploring CSV data, indexing, data manipulation, aggregation, pivot tables, and visualisation.

---

## FizzBuzz:

**Task:** Implement FizzBuzz in Python.  

**Rules:**
- Print `"FIZZ"` for numbers divisible by 3  
- Print `"BUZZ"` for numbers divisible by 5  
- Print `"FIZZBUZZ"` for numbers divisible by both 3 and 5  
- Print the number if none of the above conditions are met  

**Code Example:**
```python
for n in range(1, 101):
    if n % 3 == 0 and n % 5 == 0:
        print("FIZZBUZZ")
    elif n % 3 == 0:
        print("FIZZ")
    elif n % 5 == 0:
        print("BUZZ")
    else:
        print(n)
```
### **Output Screenshot:**
![FIZZBUZZ](FIZZBUZZ_Task/FIZZBUZZ.jpg)

### **Notebook:**
[Open FIZZBUZZ.ipynb](FIZZBUZZ_Task/FIZZBUZZ.ipynb)

---

## Student Data Analysis:

Dataset: `student.csv`

This task demonstrates 7 exercises:

**Exercise 1: Loading and Exploring the Data**

- Load CSV into Pandas DataFrame
- Display first 5 rows
- Get DataFrame info
- Get summary statistics

**Code Example:**
```python
from google.colab import drive
drive.mount('/content/drive')

import pandas as pd

df = pd.read_csv("student.csv")
df.head()
df.info()
df.describe()
```

### **Output Screenshot:**
[Click here to view Screenshots](Screenshots/W6.Q1.1.jpg)

### **Notebook:**
[Open Python_student_project.ipynb](Student.cvs_Project/Python_student_project.ipynb)





Exercise 2: Indexing and Slicing

Select columns and rows based on conditions

Code Example:

df['name']                # Select 'name' column
df[['name','mark']]       # Select 'name' and 'mark' columns
df.head(3)                # First 3 rows
df[df['class'] == 'Four'] # Rows where class = 'Four'


Screenshot:


Exercise 3: Data Manipulation

Add 'passed' column

Rename 'mark' to 'score'

Drop 'passed' column

Code Example:

df['passed'] = df['mark'] >= 60
df.rename(columns={'mark':'score'}, inplace=True)
df.drop('passed', axis=1, inplace=True)


Screenshot:


Exercise 4: Aggregation and Grouping

Group by class and calculate mean score

Count students per class

Average mark per gender

Code Example:

df.groupby('class')['score'].mean()
df['class'].value_counts()
df.groupby('gender')['score'].mean()

Exercise 5: Advanced Operations

Pivot table by class and gender

Create grade column

Sort by score descending

Code Example:

pivot = df.pivot_table(index='class', columns='gender', values='score')

def grade(score):
    if score >= 85: return 'A'
    elif score >= 70: return 'B'
    elif score >= 60: return 'C'
    else: return 'D'

df['grade'] = df['score'].apply(grade)
df.sort_values(by='score', ascending=False)

Exercise 6: Exporting Data

Save DataFrame with grades to a new CSV

Code Example:

df.to_csv("student_with_grades.csv", index=False)

Exercise 7: Visualization

Optional: create plots for marks, grades, or class distributions

Screenshot Example:


Notebook: student_analysis.ipynb

Requirements
pandas
numpy
matplotlib
seaborn


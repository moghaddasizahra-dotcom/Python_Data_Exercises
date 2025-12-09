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


## 🚀 **Objective**

- Load and analyze placement dataset (`placement.csv`)  
- Visualize the relationship between **CGPA** and **IQ** using scatter plots  
- Learn basic data exploration and visualization techniques in Python  

---

## 🛠️ **Requirements**

Make sure the following Python libraries are installed:

```python
import pandas as pd
import matplotlib.pyplot as plt
```

If any library is missing, you can install it using:

```python
!pip install pandas matplotlib
```

---

## 📊 **Dataset Description**

The dataset (`placement.csv`) contains the following columns:
- **cgpa:** Cumulative Grade Point Average of students  
- **iq:** IQ level of students  

Ensure the dataset is uploaded in the Colab environment at `/content/placement.csv`.

---

## 📝 **How to Use**

1. **Import Required Libraries:**  
   ```python
   import pandas as pd
   import matplotlib.pyplot as plt
   ```

2. **Load Dataset:**  
   ```python
   df = pd.read_csv('/content/placement.csv')
   print(df.head())
   ```

3. **Create a Scatter Plot:**  
   ```python
   plt.scatter(df['cgpa'], df['iq'])
   plt.xlabel('CGPA')
   plt.ylabel('IQ')
   plt.title('Scatter Plot of CGPA vs IQ')
   plt.show()
   ```

4. **Explore Further Analysis:**  
   - Modify and add more visualizations  
   - Perform statistical analysis  

---

## 📈 **Expected Output**

A scatter plot showing the relationship between **CGPA** and **IQ**, providing insights into how academic performance relates to intelligence levels.

## 📝 ** Steps to Achieve 90% Accuracy **
Import Required Libraries:

``` python
Copy code
import pandas as pd
import matplotlib.pyplot as plt
```
## Load the Dataset:

```python
Copy code
df = pd.read_csv('/content/placement.csv')
print("Dataset Preview:")
print(df.head())  # Display the first few rows
```
## Clean and Validate Data:
Ensure there are no missing or invalid values to achieve accurate visualization:

``` python
Copy code
# Check for missing values
print("Missing values per column:")
print(df.isnull().sum())
```

# Drop rows with missing data
df = df.dropna()

# Validate data types
``` print("\nDataset Info:")
print(df.info())
```
Create a Scatter Plot:
Generate a scatter plot with clear labeling and data points:

``` python
Copy code
plt.figure(figsize=(8, 6))
plt.scatter(df['cgpa'], df['iq'], color='blue', alpha=0.8, edgecolors='black')
plt.xlabel('CGPA', fontsize=12)
plt.ylabel('IQ', fontsize=12)
plt.title('Scatter Plot: CGPA vs IQ', fontsize=14)
plt.grid(True, linestyle='--', alpha=0.6)
plt.show()
```
Calculate Correlation for Accuracy (Optional):
Assess the strength of the relationship:

```python
Copy code
correlation = df['cgpa'].corr(df['iq'])
print(f"Correlation between CGPA and IQ: {correlation:.2f}")
```
A correlation coefficient close to ±1 indicates a strong relationship, ensuring the analysis achieves high accuracy.

## Explore Further Analysis:

Add a trendline for better visual interpretation:
``` python

import numpy as np
```

# Fit a logistics regression line
```
m, b = np.polyfit(df['cgpa'], df['iq'], 1)
plt.figure(figsize=(8, 6))
plt.scatter(df['cgpa'], df['iq'], color='blue', alpha=0.8, edgecolors='black')
plt.plot(df['cgpa'], m * df['cgpa'] + b, color='red', linestyle='--')
plt.xlabel('CGPA', fontsize=12)
plt.ylabel('IQ', fontsize=12)
plt.title('Scatter Plot with Trendline: CGPA vs IQ', fontsize=14)
plt.grid(True, linestyle='--', alpha=0.6)
plt.show()
```

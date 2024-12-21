# 100daysofML
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

---

# 📊 Univariate Analysis in EDA

Univariate Analysis is a fundamental step in **Exploratory Data Analysis (EDA)** where we analyze **a single variable at a time** to understand its distribution, central tendency, spread, and presence of outliers.

---

## 🧩 Types of Data

### 🟢 Categorical Data

Categorical variables represent **discrete groups or labels** (e.g., Gender, City, Survived).

#### 🔍 Techniques
- **Count Plot** – shows frequency of each category  
- **Bar Plot** – flexible alternative for visualization  
- **Pie Chart** – shows proportion of categories  

#### 📌 Insights
- Most frequent category (mode)  
- Class imbalance  
- Distribution across categories  

#### 💻 Example
python
import seaborn as sns
import matplotlib.pyplot as plt

sns.countplot(x=df['Survived'])
plt.show()

df['Survived'].value_counts().plot(kind='pie', autopct='%1.1f%%')
plt.show()






### 🔵 Numerical Data

Numerical variables represent **quantitative values** (e.g., Age, Salary, Price) and provide deeper insights into the dataset.

#### 🔍 Techniques
- **Histogram** – shows frequency distribution of data  
- **KDE Plot** – smooth curve to understand distribution shape  
- **Boxplot** – identifies spread and detects outliers  
- **Statistical Summary** – numerical description of data  

#### 📌 Insights
- Distribution of data (normal, skewed)  
- Central tendency (mean, median)  
- Spread (range, standard deviation)  
- Presence of outliers  
- Skewness of data  

#### 💻 Example
```python
import seaborn as sns
import matplotlib.pyplot as plt

# Histogram
sns.histplot(df['Age'], kde=True)
plt.show()

# KDE Plot
sns.kdeplot(df['Age'])
plt.show()

# Boxplot
sns.boxplot(x=df['Age'])
plt.show()

# Statistical Summary
df['Age'].describe()
df['Age'].skew()






## ⚠️ Outlier Handling

- Boxplots help in **detecting outliers**, not removing them  
- Common techniques to handle outliers:
  - Removing extreme values  
  - Capping (Winsorization)  
  - Applying transformations (log, square root)  

---

## 🧠 Skewness

- **Skewness ≈ 0** → Symmetric distribution  
- **Skewness > 0** → Right-skewed (tail on right)  
- **Skewness < 0** → Left-skewed (tail on left)  
```
---

## 📌 Summary

| Data Type    | Methods Used                         | Key Insights                      |
|-------------|-------------------------------------|----------------------------------|
| Categorical | Countplot, Barplot, Pie Chart       | Frequency, Proportion, Imbalance |
| Numerical   | Histogram, KDE, Boxplot, Statistics | Distribution, Spread, Outliers   |

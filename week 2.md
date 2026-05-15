# 📊 WEEK-02 — PANDAS, VISUALIZATION & MACHINE LEARNING
---

[View Week 2 Homework](https://github.com/rkdevesh003-hub/eos-ai-workshop/blob/main/%F0%9F%91%89WEEK%202%20HW.ipynb)

[View Random forest self study](https://github.com/rkdevesh003-hub/eos-ai-workshop/blob/main/%F0%9F%8C%B2%F0%9F%8C%B2%F0%9F%8C%B2RANDOM%20FOREST%20SELF%20STUDY%20NOTES.md)

---

# SESSION 3 · PART A · PANDAS
---

After learning NumPy, my tutors introduced Pandas.

Pandas is mainly used for:
- Data analysis
- Data cleaning
- Handling datasets
- Working with tables

For practice, we used IPL datasets.

---

# 🔹 IMPORTING PANDAS
---

```python
import pandas as pd
```

---

# 🔹 LOADING IPL DATASET
---

```python
ipl = pd.read_csv("IPL_Matches.csv")

print(ipl.head())
```

---

# 🔹 VIEWING DATA
---

```python
print(ipl.head())
print(ipl.tail())
print(ipl.info())
```

---

# 🔹 SELECTING COLUMNS
---

```python
print(ipl["Winner"])
```

```python
print(ipl[["Team1", "Team2", "Winner"]])
```

---

# 🔹 FILTERING DATA
---

```python
csk = ipl[ipl["Winner"] == "CSK"]

print(csk)
```

---

# 🔹 VALUE COUNTS
---

```python
print(ipl["Winner"].value_counts())
```

---

# 🔹 GROUPBY
---

```python
wins = ipl.groupby("Winner").size()

print(wins)
```

---

# 🔹 SORTING DATA
---

```python
sorted_data = ipl.sort_values("TotalRuns", ascending=False)

print(sorted_data.head())
```

---

# 🔹 MISSING VALUES
---

```python
print(ipl.isnull().sum())
```

```python
ipl.fillna("Unknown", inplace=True)
```

---

# 🔹 BOOLEAN MASKING
---

```python
high_scores = ipl[ipl["TotalRuns"] > 200]

print(high_scores)
```

---

# SESSION 3 · PART B · VISUALIZATION & STATISTICS
---

My tutors introduced visualization libraries like Matplotlib and Seaborn.

Visualization helps understand data in graphical form.

---

# 🔹 MATPLOTLIB
---

```python
import matplotlib.pyplot as plt
```

---

# 🔹 LINE GRAPH
---

```python
runs = [180, 190, 210, 175]
matches = [1, 2, 3, 4]

plt.plot(matches, runs)
plt.show()
```

---

# 🔹 BAR GRAPH
---

```python
teams = ["CSK", "MI", "RCB"]
wins = [25, 22, 18]

plt.bar(teams, wins)
plt.show()
```

---

# 🔹 PIE CHART
---

```python
wins = [25, 22, 18]
teams = ["CSK", "MI", "RCB"]

plt.pie(wins, labels=teams)
plt.show()
```

---

# 🌊 SEABORN
---

Seaborn is another visualization library built on top of Matplotlib.

```python
import seaborn as sns
```

---

# 🔹 COUNT PLOT
---

```python
sns.countplot(x="Winner", data=ipl)

plt.xticks(rotation=90)
plt.show()
```

---

# 🔹 HEATMAP
---

```python
correlation = ipl.corr(numeric_only=True)

sns.heatmap(correlation, annot=True)

plt.show()
```

---

# SESSION 4 · PART A · SCIKIT-LEARN
---

After learning data analysis and visualization, my tutors introduced Scikit-learn.

Scikit-learn is one of the most used Machine Learning libraries.

---

# 🔹 TRAIN TEST SPLIT
---

```python
from sklearn.model_selection import train_test_split
```

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2
)
```

---

# 🔹 LINEAR REGRESSION
---

```python
from sklearn.linear_model import LinearRegression
```

---

# 🔹 MODEL TRAINING
---

```python
model = LinearRegression()

model.fit(X_train, y_train)
```

---

# 🔹 PREDICTION
---

```python
predictions = model.predict(X_test)

print(predictions)
```

---

# SESSION 4 · PART B · CLASSIFICATION
---

Classification is a type of Machine Learning where models predict categories.

Examples:
- Spam or Not Spam
- Cat or Dog
- Positive or Negative review

---

# 🔹 LOGISTIC REGRESSION
---

```python
from sklearn.linear_model import LogisticRegression
```

---

# 🔹 ACCURACY SCORE
---

```python
from sklearn.metrics import accuracy_score
```

---

# 🔹 TRAINING CLASSIFICATION MODEL
---

```python
model = LogisticRegression()

model.fit(X_train, y_train)
```

---

# 🧠 FINAL REFLECTION — WEEK 02
---

This week helped me understand:
- Pandas
- IPL dataset analysis
- Data visualization
- Seaborn and Matplotlib
- Machine Learning basics
- Classification models

This week was very interesting because we worked with real datasets.

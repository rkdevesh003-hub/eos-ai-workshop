# 🌲 Random Forest Detailed Notes with Code Examples

---

# 📌 1. Ensemble Method

Ensemble learning means combining multiple machine learning models together to improve prediction accuracy. Instead of depending on a single Decision Tree, Random Forest creates many Decision Trees and combines their outputs.

Every tree gives its own prediction, and the final result is obtained using voting or averaging. This reduces mistakes made by individual trees.

Ensemble methods are powerful because many weak models together can create a strong model.

## 💻 Sample Code

```python
from sklearn.ensemble import RandomForestRegressor

model = RandomForestRegressor(
    n_estimators=100
)
```

## 📖 Explanation

- `RandomForestRegressor()` itself is an ensemble model.
- `n_estimators=100` means 100 decision trees are created.
- All trees work together for final prediction.

---

# 📌 2. Bagging (Bootstrap Aggregating)

Bagging means training multiple trees on different random samples of the dataset. Every tree receives a slightly different version of the training data.

Because of this:
- each tree learns differently
- each tree makes different mistakes

When all predictions are combined, the overall model becomes more stable and accurate.

Bagging mainly helps in reducing:
- overfitting
- variance in Decision Trees

## 💻 Sample Code

```python
from sklearn.ensemble import RandomForestRegressor

model = RandomForestRegressor(
    n_estimators=100,
    bootstrap=True
)
```

## 📖 Explanation

- `bootstrap=True` enables bagging.
- Random samples are selected for each tree.
- Different trees see different data.

---

# 📌 3. Difference Between Decision Tree and Random Forest

A Decision Tree uses only one tree structure for prediction, while Random Forest uses many trees together.

A single Decision Tree may:
- overfit training data
- produce unstable predictions

Random Forest solves this by combining multiple trees and averaging their predictions.

Decision Trees are simpler and faster, but Random Forest is more accurate and reliable.

## 🌳 Decision Tree Code

```python
from sklearn.tree import DecisionTreeRegressor

tree_model = DecisionTreeRegressor()
```

## 🌲 Random Forest Code

```python
from sklearn.ensemble import RandomForestRegressor

forest_model = RandomForestRegressor(
    n_estimators=100
)
```

## 📖 Explanation

- Decision Tree → one tree
- Random Forest → many trees
- Random Forest gives better generalization

---

# 📌 4. Feature Randomness

Feature randomness means Random Forest randomly selects some features during each split.

Not all features are checked every time.

This makes trees different from each other and prevents all trees from making the same mistakes.

Random feature selection:
- increases diversity among trees
- improves model performance
- reduces correlation between trees

## 💻 Sample Code

```python
from sklearn.ensemble import RandomForestRegressor

model = RandomForestRegressor(
    max_features="sqrt"
)
```

## 📖 Explanation

- `max_features="sqrt"` selects random features.
- If there are 16 features, only 4 random features are checked.
- Every tree uses different feature combinations.
- Helps reduce overfitting.

---

# 📌 5. Majority Voting and Averaging

Random Forest combines outputs from all trees.

## 🗳️ Classification → Majority Voting

In classification problems:
- the class predicted by most trees becomes the final answer

### 💻 Classification Code

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=100
)

model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```

### 📖 Explanation

- Each tree predicts a class.
- Majority voting gives the final answer.

---

## 📊 Regression → Averaging

In regression problems:
- predictions from all trees are averaged

### 💻 Regression Code

```python
from sklearn.ensemble import RandomForestRegressor

model = RandomForestRegressor(
    n_estimators=100
)

model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```

### 📖 Explanation

- All tree outputs are averaged.
- Averaging reduces extreme predictions.
- Final prediction becomes more stable.

---

# 📌 6. Hyperparameters

Hyperparameters are settings provided before training the model.

They control:
- model behavior
- accuracy
- speed
- overfitting

Important hyperparameters include:
- `n_estimators`
- `max_depth`
- `max_features`
- `bootstrap`

## 💻 Sample Code

```python
from sklearn.ensemble import RandomForestRegressor

model = RandomForestRegressor(
    n_estimators=100,
    max_depth=5,
    max_features="sqrt",
    bootstrap=True
)
```

## 📖 Explanation

### 🔹 n_estimators

```python
n_estimators=100
```

This parameter decides how many Decision Trees should be created inside the Random Forest model.

---

### 🔹 max_depth

```python
max_depth=5
```

This parameter controls the maximum depth of each Decision Tree and helps reduce overfitting.

---

### 🔹 max_features

```python
max_features="sqrt"
```

This parameter determines how many random features are selected at each split.

If the dataset has 16 features:
- only 4 random features are checked at a split

This increases randomness and reduces overfitting.

---

### 🔹 bootstrap

```python
bootstrap=True
```

This parameter enables bagging by allowing each tree to train on random samples of the dataset.

---

# 📌 7. Feature Importance

Feature importance tells which features contribute most to predictions.

Random Forest calculates importance scores for every feature.

Features with high scores:
- influence predictions more strongly
- are more useful for the model

Feature importance helps in:
- understanding datasets
- feature selection
- data analysis

## 💻 Sample Code

```python
importance = model.feature_importances_

print(importance)
```

---

## 📊 Better Table Format

```python
import pandas as pd

feature_table = pd.DataFrame({
    "Feature": X.columns,
    "Importance": model.feature_importances_
})

print(feature_table.sort_values(
    by="Importance",
    ascending=False
))
```

## 📖 Explanation

- Shows most important columns
- Helps in feature selection
- Useful for interpretation

---

# 📌 8. Strengths and Weaknesses of Random Forest

Random Forest has many advantages compared to Decision Trees.

It:
- provides high accuracy
- reduces overfitting
- works well on large datasets
- supports regression and classification

However:
- training is slower
- memory usage is higher
- visualization becomes difficult

## 💻 Sample Code

```python
from sklearn.ensemble import RandomForestRegressor

model = RandomForestRegressor(
    n_estimators=200,
    max_depth=10
)
```

---

## ✅ Strengths

- High accuracy
- Less overfitting
- Handles large datasets
- Supports regression and classification

---

## ❌ Weaknesses

- Slower training
- More memory usage
- Harder to visualize

---

# 🚀 Complete Random Forest Code

```python
import pandas as pd
import numpy as np

from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import (
    mean_absolute_error,
    mean_squared_error,
    r2_score
)

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)

# Create Random Forest model
model = RandomForestRegressor(
    n_estimators=100,
    max_depth=5,
    max_features="sqrt",
    bootstrap=True,
    random_state=42
)

# Train model
model.fit(X_train, y_train)

# Make predictions
y_pred = model.predict(X_test)

# Evaluation Metrics
mae = mean_absolute_error(y_test, y_pred)

mse = mean_squared_error(y_test, y_pred)

rmse = np.sqrt(mse)

r2 = r2_score(y_test, y_pred)

print("MAE:", mae)
print("MSE:", mse)
print("RMSE:", rmse)
print("R2 Score:", r2)

# Feature Importance
feature_table = pd.DataFrame({
    "Feature": X.columns,
    "Importance": model.feature_importances_
})

print(feature_table.sort_values(
    by="Importance",
    ascending=False
))
```

---

# 🎯 Final Conclusion

Random Forest is a powerful ensemble learning algorithm that combines multiple Decision Trees using:
- bagging
- feature randomness
- averaging
- majority voting

This improves:
- accuracy
- stability
- generalization

while reducing overfitting.

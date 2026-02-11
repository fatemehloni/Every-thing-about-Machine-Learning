# Summary of *Intro to Machine Learning*

**Course:** Kaggle – Intro to Machine Learning  
**Scope:** Foundational supervised learning concepts using Python, Pandas, and Scikit-learn  

---

## 1. Introduction to Supervised Learning and Decision Trees

This course introduces supervised learning through **Decision Tree Regression**, a non-parametric predictive modeling approach.

A decision tree recursively partitions the feature space into subsets based on decision rules derived from input variables. Each internal node represents a split condition, and each terminal node—called a **leaf**—represents a prediction.

Conceptually:

- The dataset is divided through hierarchical binary splits.
- Each split aims to reduce prediction error.
- The final prediction is generated at a leaf node.

> The terminal node of a decision tree where a prediction is produced is called a *leaf*.

Decision trees are interpretable and serve as a foundational model for understanding predictive learning systems.

---

## 2. Data Representation with Pandas

The course emphasizes structured data handling using the **Pandas** library.

### Core Data Structures

- **DataFrame**: A two-dimensional tabular structure (rows × columns).
- **Series**: A one-dimensional labeled array (typically a single column).

Pandas enables:

- Dataset loading
- Exploratory data inspection
- Descriptive statistical summaries
- Column-based selection for modeling

Structured data representation forms the basis of machine learning pipelines.

---

## 3. Feature Selection and Target Definition

In supervised learning, datasets are separated into:

- **Prediction Target (y)**
- **Feature Matrix (X)**

### 3.1 Prediction Target

The prediction target is the dependent variable to be estimated.


Example:

```python
y = melbourne_data.Price
```

This creates a Pandas Series representing the outcome variable.

---

### 3.2 Feature Matrix

Features are explanatory variables used to predict the target.

\[
X = \{x_1, x_2, ..., x_n\}
\]

Example:

```python
melbourne_features = ['Rooms', 'Bathroom', 'Landsize', 'Lattitude', 'Longtitude']
X = melbourne_data[melbourne_features]
```

Feature selection influences model capacity and generalization performance.

---

## 4. Model Construction Using Scikit-learn

The modeling workflow follows four structured steps:

1. **Define**  
   Select model type and specify hyperparameters.

2. **Fit**  
   Train the model on provided data.

3. **Predict**  
   Generate predictions.

4. **Evaluate**  
   Measure predictive performance.

Scikit-learn provides a standardized API for implementing this pipeline efficiently.

---

## 5. Model Validation and Predictive Evaluation

### 5.1 The Importance of Validation

Evaluating a model using the same dataset employed for training results in an **in-sample score**, which often overestimates real-world performance.

Models may capture dataset-specific noise rather than generalizable patterns.

To estimate practical predictive ability, evaluation must occur on unseen data.

---

### 5.2 Mean Absolute Error (MAE)

One metric introduced in the course is **Mean Absolute Error (MAE)**:
MAE measures the average magnitude of prediction errors.

Interpretation:

> On average, predictions deviate from actual values by approximately X units.

---

### 5.3 Validation Data

To obtain an unbiased estimate of performance:

- Split dataset into:
  - Training set
  - Validation set

Model training is performed on the training data.  
Performance evaluation is conducted on validation data that the model has not previously seen.

---

## 6. Bias–Variance Tradeoff: Underfitting and Overfitting

A central concept in machine learning is balancing model complexity and generalization.

### 6.1 Tree Depth and Model Complexity

In decision trees, complexity increases with the number of splits.

### 6.2 Overfitting

Occurs when:

- The model is excessively complex.
- Leaves contain very few observations.
- The model memorizes training data patterns.

Consequences:

- Low training error
- High validation error

---

### 6.3 Underfitting

Occurs when:

- The model is too simple.
- Important structural patterns are not captured.

Consequences:

- High training error
- High validation error

---

### 6.4 Controlling Model Complexity

The hyperparameter:

```python
max_leaf_nodes
```

controls the number of terminal nodes.

Increasing the number of leaves:

- Reduces bias
- Increases variance

Optimal performance lies between underfitting and overfitting.

---

## 7. Ensemble Learning: Random Forest

The course introduces **Random Forest**, an ensemble learning method.

A random forest:

- Builds multiple decision trees
- Trains each tree on randomized subsets of data/features
- Aggregates predictions (typically by averaging)

Advantages:

- Reduced variance compared to a single tree
- Improved generalization
- Stable performance with default parameters

Random Forest demonstrates how combining multiple weak learners can yield stronger predictive performance.

---

## 8. Conceptual Outcomes

This course establishes foundational competencies in:

- Structured data manipulation
- Supervised regression modeling
- Model evaluation methodology
- Bias–variance tradeoff
- Basic ensemble techniques

It provides a structured introduction to predictive modeling within the Scikit-learn ecosystem.

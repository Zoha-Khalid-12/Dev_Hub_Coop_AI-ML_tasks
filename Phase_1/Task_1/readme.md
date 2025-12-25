# Iris EDA + Baseline Classification

## Task Objective
Explore the Iris dataset using pandas, matplotlib, and seaborn to understand feature distributions and relationships, then train and evaluate a baseline machine learning model to classify Iris flower species.

## Dataset Used
**Iris Dataset** (loaded via `seaborn.load_dataset("iris")`)

- **Rows:** 150  
- **Features (4 numeric):**
  - `sepal_length`, `sepal_width`, `petal_length`, `petal_width`
- **Target (categorical):**
  - `species` (setosa, versicolor, virginica)
- **Preprocessing:**
  - Checked missing values (typically none)
  - Standardized numeric features using `StandardScaler` (via sklearn Pipeline)

## Models Applied
1. **Logistic Regression (Baseline Classifier)**
   - Implemented as an sklearn `Pipeline`:
     - `StandardScaler()` → `LogisticRegression(max_iter=1000)`

## Key Results and Findings

### Data Exploration (EDA) Insights
- **Petal features** (`petal_length`, `petal_width`) show the strongest separation between species.
- **Setosa** is usually clearly separable from the other two classes.
- **Versicolor vs Virginica** tend to overlap more, making them the most common source of misclassification (if any).

### Model Performance (Typical Outcome)
- Logistic Regression on Iris generally achieves **high accuracy** on a standard train/test split.
- Errors (if present) mostly occur between **versicolor** and **virginica**.

### Final Takeaways
- The Iris dataset is clean and well-suited for practicing EDA and baseline classification.
- Simple linear models already perform very well due to strong feature separability, especially with standardized features.

## How to Run
1. Open the Jupyter Notebook.
2. Run cells top to bottom:
   - Load & inspect data
   - Visualize distributions/relationships
   - Train model
   - Evaluate results (accuracy, classification report, confusion matrix)

## Next Steps (Optional)
- Compare multiple models (KNN, SVM, Random Forest) using cross-validation.
- Add hyperparameter tuning (GridSearchCV).
- Explore feature importance (coefficients for Logistic Regression).

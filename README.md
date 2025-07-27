# 🌲 Forest Cover Type Prediction using XGBoost

This project focuses on building a machine learning model to classify forest cover types using cartographic variables from the **UCI Forest CoverType Dataset**. The model leverages **XGBoost** — an efficient and scalable gradient boosting framework — and includes **hyperparameter tuning** with `RandomizedSearchCV`, as well as preprocessing, evaluation, and visualization.

---

## 📌 Objectives

- Predict the type of forest cover for a given patch of land.
- Explore and preprocess the dataset effectively.
- Train a robust model using **XGBoost**.
- Tune hyperparameters using cross-validation techniques.
- Evaluate model performance using multiple metrics and visualizations.

---

## 📊 Dataset

- **Source**: [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/Covertype)
- **Rows**: 581,012
- **Features**: 54 (10 numerical + 44 binary categorical)
- **Target**: `Cover_Type` (7 classes from 1 to 7, each representing a forest type)

---

## 🧪 Features Used

- Elevation, Aspect, Slope
- Horizontal & Vertical distances to hydrology, roadways, and fire points
- Hillshade at different times of day
- Wilderness Area and Soil Type (one-hot encoded)

---

## ⚙️ ML Workflow

1. **Data Exploration & Cleaning**
   - Handled invalid labels
   - Checked class distribution and data quality

2. **Feature Engineering**
   - Applied standardization / normalization as needed
   - Dropped zero-variance features (if any)

3. **Model Training**
   - Base XGBoost model training
   - Evaluation with Accuracy, F1-score, Confusion Matrix

4. **Hyperparameter Tuning**
   - `RandomizedSearchCV` to efficiently explore wide ranges
   - `GridSearchCV` for final fine-tuning

5. **Model Evaluation**
   - Detailed classification report
   - Visual analysis (confusion matrix, feature importances)

---

## 🧠 Model Details

- **Algorithm**: XGBoost Classifier (`xgboost.XGBClassifier`)
- **Hyperparameters Tuned**:
  - `n_estimators`
  - `max_depth`
  - `learning_rate`
  - `subsample`, `colsample_bytree`
  - `min_child_weight`, `gamma`

---

## 📈 Results

- Achieved high accuracy on the test set.
- Balanced performance across all 7 cover types.
- XGBoost performed significantly better than baseline models.

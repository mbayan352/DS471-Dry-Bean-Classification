DS471 Machine Learning Project: Dry Bean Classification

Project Overview

This project applies machine learning techniques to classify dry bean varieties based on their physical characteristics.

The main objective is to develop and compare traditional machine learning models and a Neural Network to identify the most suitable model for the classification task.

Dataset

The project uses the Dry Bean Dataset from the UCI Machine Learning Repository.

- Original samples: 13,611
- Features: 16 numerical features
- Target variable: "Class"
- Number of classes: 7
- Samples after removing duplicates: 13,543

The seven bean classes are:

- Barbunya
- Bombay
- Cali
- Dermason
- Horoz
- Seker
- Sira

Data Preparation

The following preparation steps were performed:

- Checked for missing values and duplicate records.
- Removed 68 duplicate rows.
- Examined feature distributions and outliers.
- Performed exploratory data analysis (EDA).
- Analyzed feature correlations.
- Applied stratified data splitting.
- Used StandardScaler for models that require feature scaling.

Data Splitting

The cleaned dataset was divided into three subsets:

Dataset| Samples| Ratio
Training| 9,480| 70%
Validation| 2,031| 15%
Testing| 2,032| 15%

A stratified split was used to maintain class distribution across the three subsets.

Machine Learning Models

Four classification models were developed and evaluated:

1. Logistic Regression
2. Support Vector Machine (SVM) with an RBF kernel
3. Random Forest
4. Neural Network (MLP)

Hyperparameter Optimization

Model optimization included:

- 5-fold cross-validation for traditional machine learning models.
- Hyperparameter comparison for the Neural Network using the validation set.
- Dropout and Early Stopping to help control overfitting.

The selected Neural Network architecture was:

"16 → 64 → 32 → 7"

It used a dropout rate of 0.2 and a learning rate of 0.001.

Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- Macro F1-score
- Confusion Matrix

Macro F1-score was selected as the main metric because the dataset contains imbalanced classes.

Final Test Results

Model| Accuracy| Macro F1-score
SVM| 0.9232| 0.9361
Neural Network| 0.9222| 0.9352
Logistic Regression| 0.9218| 0.9347
Random Forest| 0.9168| 0.9307

The SVM achieved the highest test Macro F1-score (0.9361), followed closely by the Neural Network (0.9352).

Tools and Libraries

- Python
- Google Colab / Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- TensorFlow / Keras

How to Run the Project

1. Open the project notebook in Google Colab or Jupyter Notebook.
2. Run the notebook cells in order.
3. The notebook automatically attempts to download the Dry Bean dataset.
4. Install any required libraries if they are not already available.
5. Execute the complete workflow, from data preparation to final model evaluation.

Project Structure

The repository contains the project notebook and relevant project files.

Course Information

Course: DS471 – Machine Learning
Project: Dry Bean Classification

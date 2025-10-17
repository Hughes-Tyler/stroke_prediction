# Stroke Prediction Modeling Project

## Overview
This project builds and evaluates several machine learning models to predict the likelihood of a patient having a stroke.  
All work was done using Python and scikit-learn in a Jupyter Notebook.

## Modeling Pipeline
1. Loaded and explored the dataset from `RawData/train.csv`.
2. Cleaned data and handled categorical encoding using `pd.get_dummies()`.
3. Split the dataset into training (80%) and testing (20%) sets.
4. Trained three models:
   - **Logistic Regression**
   - **Logistic Regression (Cross-Validation)**
   - **K-Nearest Neighbors (KNN)**
5. Evaluated each model using:
   - Accuracy  
   - Precision  
   - Recall  
   - F1-Score  
   - Confusion Matrix Visualization  
6. Generated final predictions for the test set (`RawData/test.csv`) and saved results in the `Output/` folder.

## Algorithms Used
- **Logistic Regression:** baseline linear classifier.  
- **Logistic RegressionCV:** includes built-in cross-validation and automatic regularization tuning.  
- **KNN:** non-parametric model; included for comparison.
  # Results are shown in main.ipynb under the code folder

## Kaggle Results
Final submission achieved a **score of 0.24** on the Kaggle leaderboard.  
While not among the top results, it was a solid outcome given that we were limited to the techniques covered so far.

## Reflections
This project taught me a lot about building a full ML workflow end-to-end.  
I really enjoyed getting close to the data, using simple models for classification, and seeing how I compared to others in the Kaggle leaderboard. 
Seeing the high leaderboard scores was motivating — it’s clear that there’s a lot more to explore in data cleaning, feature engineering, and ensemble methods.

---

**Folder Guide**
- `Code/` – Jupyter notebooks and scripts  
- `RawData/` – Original datasets  
- `ProcessedData/` – Cleaned or transformed data (if created)  
- `Output/` – Model predictions and evaluation results  
- `requirements.txt` – Required packages  
- `README.md` – Summary of the workflow

<img width="1212" height="215" alt="image" src="https://github.com/user-attachments/assets/795c719f-c9b2-43c2-ad3b-2fd27059c37a" />

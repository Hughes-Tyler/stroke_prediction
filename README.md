# Stroke Prediction Modeling Project

## Overview
This project builds and evaluates several machine learning models to predict the likelihood of a patient having a stroke.  
All work was done in Python using **scikit-learn** inside a **Jupyter Notebook**. The main goal was to understand how different classification models perform not just based on accuracy, but on their ability to correctly identify true stroke cases.

---

## Modeling Pipeline
1. Loaded and explored the dataset from `RawData/train.csv`.  
2. Cleaned and encoded categorical variables using `pd.get_dummies()`.  
3. Split the data into an **80/20 training and testing set**.  
4. Trained three models:  
   - **Logistic Regression**  
   - **Logistic Regression with Cross-Validation (LogisticRegressionCV)**  
   - **K-Nearest Neighbors (KNN)**  
5. Evaluated each using:
   - Accuracy  
   - Precision  
   - Recall  
   - F1 Score  
   - Confusion Matrix heatmaps for visualization  
6. Generated predictions on the test set (`RawData/test.csv`) and saved them in the `Output/` folder.

---

## Model Results

| Model | Accuracy | Precision | Recall | F1 Score |
|:------|:----------:|:-----------:|:---------:|:----------:|
| Logistic Regression | 0.9539 | 0.4444 | 0.0357 | 0.0661 |
| **Logistic RegressionCV** | 0.7922 | 0.1572 | **0.8125** | **0.2634** |
| K-Nearest Neighbors | 0.9518 | 0.3636 | 0.0714 | 0.1194 |

At first glance, the Logistic Regression and KNN models look great because of their high accuracy (around 95%), but that number doesn’t tell the full story. The dataset is **highly imbalanced**, meaning very few people in the data actually had a stroke. This means that even if the model only predicted “no stroke”, it will still seem accurate even though it fails to catch the positive cases.

That’s where **recall** becomes critical. Recall measures how many actual stroke cases our model successfully identified.  
The **Logistic Regression CV** model stood out here with a recall of **0.81**, meaning it caught most of the true stroke cases. Even though its precision and accuracy were lower, that trade-off is completely worth it in this kind of medical context. Missing a real stroke case could be much worse than flagging a few false positives.

Overall, **Logistic Regression CV** was the best-performing model because it prioritized the right metric for this problem.

---

## Kaggle Results
My final Kaggle submission achieved a **score of 0.24**.  
Not a leaderboard-topping result, but considering we were limited to only the concepts we’ve learned so far, I’m happy with the progress. Seeing how much feature engineering, resampling, and model tuning can boost results has been a great motivator for future projects.

---

## Reflections
This project really helped me connect the dots between metrics and meaning. I used to think a high accuracy automatically meant a good model. Now I know that with imbalanced data, **accuracy can be misleading**. Precision and recall tell a more complete story, especially when the cost of missing positive cases is high.

I also liked how **Logistic Regression CV** handled cross-validation and regularization automatically — it gave much stronger recall without any manual tuning.  
**KNN**, on the other hand, was my least favorite. It struggled with scaling and class imbalance, and the metrics showed it.

Seeing the Kaggle leaderboard was a good reality check. There’s a big gap between basic models and tuned, production-level ones. That gap is exactly what I want to close in future work.

---

## Folder Guide
- `Code/` – Jupyter notebook (`main.ipynb`) containing all code and visualizations  
- `RawData/` – Original training and test datasets  
- `ProcessedData/` – Any cleaned or transformed data (optional)  
- `Output/` – Predictions and evaluation outputs  
- `requirements.txt` – List of Python dependencies  
- `README.md` – Project summary and reflections  

---
<img width="1215" height="544" alt="image" src="https://github.com/user-attachments/assets/678101d2-a245-4d2f-aea5-3d23b6305f4c" />


*Boston College – Big Data Econometrics (HW2)*  

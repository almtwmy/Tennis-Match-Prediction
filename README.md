# 🎾 Tennis Match Winner Prediction

## 📚 Project Overview
This project aims to predict the winner of a tennis match **before** it happens, using only **pre-match information** such as player rankings, age, height, handedness, tournament details, and more.  
It was developed as part of the **ICS 574 - Big Data Analytics** course under the supervision of **Dr. Mustafa Ghaleb**.

---

## 🎯 Goal
Build a machine learning model that predicts whether **Player 1 wins (target = 1)** or **Player 2 wins (target = 0)** using structured match data.

---

## 🛠 Project Steps
### 1. Data Cleaning
- Handling missing values.
- Correcting data types.

### 2. Data Transformation
- Rename `winner_*` → `p1_*`, `loser_*` → `p2_*` to avoid bias.
- Add `target` column (1 if Player 1 wins).
- Duplicate and flip the match rows to balance the dataset.

### 3. Feature Engineering
- Encoding categorical features (One-Hot Encoding).
- Scaling numerical features (StandardScaler).
- Adding new features: Player historical win counts.

### 4. Modeling
- Training different machine learning models:
  - Logistic Regression
  - K-Nearest Neighbors (on 10% sample)
  - Random Forest Classifier
  - SGD Classifier
  - Decision Tree Classifier

### 5. Evaluation
- Comparing model performance (Training vs Test Accuracy).
- Measuring the improvement after adding new features.

---

## 🧠 Models and Results

| Model                          | Training Accuracy (%) | Test Accuracy (%) |
|:-------------------------------|:----------------------:|:-----------------:|
| Logistic Regression            | 65.71%                 | 65.58%            |
| K-Nearest Neighbors (10% Sample)| 73.63%                 | 59.26%            |
| Random Forest Classifier       | 100.00%                | 65.57%            |
| SGD Classifier                 | 65.18%                 | 65.26%            |
| Decision Tree Classifier       | 100.00%                | 58.74%            |

✅ **Best overall model:** Logistic Regression and Random Forest after feature engineering.

---

## 🔥 Challenges Faced
- Handling very large datasets efficiently (~1 million rows).
- Balancing the dataset to avoid prediction bias toward the original winner.
- Scaling KNN and SVC models on large datasets (required subsampling).

---

## 🌟 Future Recommendations
- Try more complex models (e.g., XGBoost, LightGBM).
- Hyperparameter tuning for Random Forest and Decision Trees.
- Add more dynamic features (like recent form, head-to-head statistics).
- Explore deep learning if more features and computing power are available.

## Data Source and License

The tennis match data used in this project is provided by [Jeff Sackmann / Tennis Abstract](https://github.com/JeffSackmann/tennis_atp).

This dataset is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

This project is for **academic and non-commercial purposes** only.



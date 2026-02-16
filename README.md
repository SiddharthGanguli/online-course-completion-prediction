# Online Course Completion Prediction

This project analyzes user engagement data from an online learning platform to predict whether a student will complete a course using machine learning models.

---

##  Dataset

**Source:**  
https://www.kaggle.com/datasets/muqaddasejaz/online-course-engagement-dataset

- **Rows:** 9,000  
- **Columns:** 9  
- **Target:** `CourseCompletion`  
  - `0` → Not Completed (48%)  
  - `1` → Completed (52%)

The dataset is well-balanced, making it suitable for classification modeling.

---

##  Features

### Numerical Features
- `TimeSpentOnCourse`
- `NumberOfVideosWatched`
- `NumberOfQuizzesTaken`
- `QuizScores`
- `CompletionRate`

### Categorical Features
- `CourseCategory`
- `DeviceType`

---

##  What Was Done

###  Data Preprocessing
- Removed `UserID`
- Built preprocessing pipeline using:
  - `StandardScaler` (for numerical features)
  - `OneHotEncoder` (for categorical features)
  - `ColumnTransformer`
- Created an end-to-end `Pipeline`

###  Model Evaluation
- Implemented **5-Fold Cross-Validation**
- Compared two models:
  - Logistic Regression (baseline)
  - Random Forest Classifier

---

##  Results

### Logistic Regression
- **Mean Accuracy:** ~80%

### Random Forest
- **Mean Accuracy:** ~96%
- Strong and stable performance across folds

###  Key Insights
Feature importance analysis shows that course completion is mainly driven by:
- `CompletionRate`
- `QuizScores`
- Student activity levels (videos watched, quizzes taken)

Engagement metrics are the strongest predictors of completion.

---

##  Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

##  Project Type

Supervised Machine Learning  
Binary Classification  

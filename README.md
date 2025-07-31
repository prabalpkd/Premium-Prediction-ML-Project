# 🏥 Health Insurance Premium Prediction using Machine Learning

This project predicts **Medical Insurance Premiums** based on demographic, health, and lifestyle factors using advanced machine learning techniques. It includes thorough EDA, model experimentation, hyperparameter tuning, segmentation-based modeling, and an interactive **Streamlit app** for real-time predictions.

![App Screenshot](./Screenshot%202025-07-31%20091949.png)

---

## 📌 Highlights

- 📊 In-depth Exploratory Data Analysis (EDA) with univariate and bivariate visualizations.
- 🔍 Regression model experimentation: **Linear Regression**, **Lasso**, **Ridge**, and **XGBoost**.
- 🧪 Hyperparameter tuning with **RandomizedSearchCV** for optimal XGBoost performance.
- 🧑‍⚕️ **Segmented modeling**: separate models for age groups to improve prediction performance.
- 🌐 Streamlit-based frontend app with sliders and dropdowns for intuitive use.

---

## 🧾 Problem Statement

The goal is to build a robust regression model that can predict the **medical insurance premium** for individuals based on:
- Demographics (age, gender, region, etc.)
- Health indicators (BMI category, genetic risk, medical history)
- Lifestyle (smoking status)
- Economic factors (income, employment status)

---

## 📁 File Structure

```bash
.
├── MedIns_Premium_prediction.ipynb                  # Full EDA + Base Models + Tuning
├── MedIns_Premium_prediction_Young_with_Gr.ipynb    # Model trained for young population (age ≤ 25)
├── MedIns_Premium_prediction_rest_with_Gr.ipynb     # Model trained for rest of the population (age > 25)
├── Screenshot 2025-07-31 091949.png                 # Streamlit app UI preview
├── app/                                             # (Optional) Streamlit app code folder
└── README.md                                        # You are here!
```
📊 Exploratory Data Analysis (EDA)
1. Conducted extensive EDA using:
2. Distribution plots of numeric variables (age, income, genetical risk)
3. Count plots for categorical variables (region, smoking status, BMI category)
4. Correlation heatmap and VIF to handle multicollinearity
5. Outlier handling and feature transformation

🧠 Model Development
Multiple regression models were evaluated:

| Model             | Technique Used         | Notes                        |
| ----------------- | ---------------------- | ---------------------------- |
| Linear Regression | Baseline Model         | Simple, interpretable        |
| Lasso/Ridge       | Regularized Regression | Tested for multicollinearity |
| XGBoost Regressor | Ensemble Learning      | Best performance             |

✅ XGBoost was tuned using RandomizedSearchCV with parameters like n_estimators, learning_rate, and max_depth.

🔀 Segmentation Strategy

The model showed lower R² performance for young individuals (≤ 25 years). To address this:

Split the dataset into:

  1. Young Group: Age ≤ 25
  2. Rest Group: Age > 25

Trained separate XGBoost models for each group.

Final deployment uses the appropriate model based on age input from the user.

This segmentation significantly improved prediction accuracy and model reliability.


🌐 Streamlit App
A clean and responsive app was built using Streamlit to serve predictions.

🔧 Features:
1. Numeric sliders for age, income, genetical risk, dependents
2. Dropdowns for categorical variables like gender, region, etc.
3. Predict button returns real-time estimated premium

🔍 Input Features
   age, number of dependents, income

   genetical risk, gender, smoking status

   BMI category, insurance plan, region

   employment status, marital status, medical history


⚙️ Tech Stack
1. Language: Python
2. ML Libraries: scikit-learn, XGBoost
3. Visualization: Matplotlib, Seaborn
4.App Framework: Streamlit

📈 Model Evaluation Metric
1. R² Score (Coefficient of Determination)
2. Mean Absolute Error (MAE)
3. Mean Squared Error (MSE)

📌 Key Learnings
1. Handling of feature segmentation based on demographic insights
2. Importance of domain understanding in improving model performance
3. Streamlit for real-time model deployment

🙋 About Me
Prabal Kumar Deka
🎓 Data Science & Machine Learning Enthusiast

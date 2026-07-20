# Medical Insurance Cost Prediction

## 🎯 Objective
Develop a **Multiple Linear Regression** model to predict individual medical insurance charges using demographic and health‑related factors. The project highlights how personal attributes influence medical costs and supports insurance underwriting decisions.

---

## 📊 Dataset
- **Source:** [Kaggle – Medical Cost Personal Insurance Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)  
- **Target Variable:** `charges` (continuous numerical value)  
- **Features:**  
  - **Numerical:** `age`, `bmi`, `children`  
  - **Categorical:** `sex`, `smoker`, `region`  

---

## 🛠️ Libraries Used
- **pandas** → data handling & preprocessing  
- **numpy** → numerical operations  
- **scikit‑learn** → train/test split, regression model, evaluation metrics  
- **matplotlib** → visualization (scatter plots)  
- **seaborn** → enhanced statistical plotting  

---

## 🔎 Methodology
1. **Data Understanding**  
   - Loaded dataset, inspected first records, identified numerical/categorical features.  

2. **Preprocessing**  
   - Checked for missing values.  
   - Encoded categorical variables (`sex`, `smoker`, `region`) using one‑hot encoding.  
   - Split dataset into **80% training** and **20% testing**.  

3. **Model Development**  
   - Built a Multiple Linear Regression model using features: `age`, `bmi`, `children`, `sex`, `smoker`, `region`.  
   - Trained on training set and predicted charges for test set.  

4. **Evaluation**  
   - Metrics: **MAE**, **MSE**, **R² Score**.  
   - Visualized results with **Actual vs Predicted scatter plot**.  

---

## 📈 Results
- **R² Score:** ~0.78  
- **MAE:** ~4,180  
- **RMSE:** ~5,790  

**Observations:**  
- Smoking status is the strongest driver of higher charges.  
- Age and BMI also significantly influence costs.  
- Region and gender show minimal impact.  
- Scatter plot indicates some non‑linear patterns beyond linear regression’s scope.  

---

## 📝 Conclusion
The regression model explains around **78% of the variance** in medical costs, confirming that **smoking, age, and BMI** are the most critical predictors. While effective for identifying major cost drivers, linear regression has a key limitation: it assumes purely additive, independent effects. This means it cannot naturally capture complex interactions (e.g., high BMI combined with smoking) without explicitly engineering interaction terms.

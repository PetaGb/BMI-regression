# 🧠 Obesity Risk Prediction (BMI Regression)

This project predicts **Body Mass Index (BMI)** based on individuals’ **eating habits, lifestyle**, and **demographics** using data from **Mexico, Peru, and Colombia**.  
The dataset contains **2,111 records** and **17 features** describing habits such as diet, activity level, and technology use.

---

## 🎯 Objective

The original dataset classified individuals into seven obesity levels (`NObesity`).  
I replaced this categorical label with a **continuous BMI variable**, enabling **regression-based modelling** — a more direct and interpretable approach to obesity prediction.

---

## 📊 Features

| Feature | Description |
|----------|-------------|
| `FAVC` | Frequent consumption of high-caloric food |
| `FCVC` | Frequency of vegetable consumption |
| `NCP` | Number of main meals per day |
| `CAEC` | Eating between meals |
| `CH2O` | Daily water consumption |
| `CALC` | Alcohol consumption |
| `SMOKE` | Smoking status |
| `SCC` | Calorie monitoring |
| `FAF` | Physical activity frequency |
| `TUE` | Time using technology |
| `MTRANS` | Mode of transportation |
| `family_history_with_overweight`, `Age`, ... | Demographics |

---

## ⚙️ Modeling

- **Linear models** performed **very poorly**, as expected — overall correlations between variables were low.  
- **Ensemble models** captured relationships far better.  
  - **Random Forest** slightly outperformed **Gradient Boosting** (87% vs 82%) while being simpler.  
  - A minimal gap between **R²** and **CV scores** indicates **strong generalization**.

---

## 📈 Results

| Metric | Result |
|--------|---------|
| BMI ±20% Accuracy | **92%** |
| BMI ±10% Accuracy | **78.5%** |
| Largest Error | Real BMI **44** → Predicted **29** |

---

## 🔍 Key Insights

- Most predictions are close to actual BMI, with a few notable outliers.  
- Top predictors:  
  1. `family_history_with_overweight`  
  2. `vegetable_consumption_freq`
  3. `Age` (less reliable >50 due to limited samples)

- Predictions for people **over 50** may be less reliable.

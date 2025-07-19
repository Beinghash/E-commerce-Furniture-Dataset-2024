# 🪑 E-commerce Furniture Dataset Analysis (2024)

![project-banner](https://img.shields.io/badge/Project-Type-Data%20Analysis-blue)
![language](https://img.shields.io/badge/Python-3.9%2B-green)
![status](https://img.shields.io/badge/Status-Completed-brightgreen)
![license](https://img.shields.io/badge/License-MIT-lightgrey)

This project explores and analyzes a dataset of furniture products scraped from AliExpress.  
The objective is to **predict the number of units sold** based on product attributes like price, title, and shipping tags using regression models.

---

## 📌 Project Objective

> Predict the `sold` count of furniture products using the following features:
- `productTitle` (text)
- `originalPrice`
- `price`
- `tagText` (shipping info)

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Jupyter Notebook | IDE for development & visualization |
| pandas | Data loading & manipulation |
| seaborn, matplotlib | Data visualization |
| scikit-learn | Machine learning models |
| TfidfVectorizer | Text vectorization of product titles |

---

## 📊 Project Workflow

1. **Data Preprocessing**  
   - Cleaned `price`, dropped rows with missing values  
   - Converted `tagText` to numeric `shipping_cost`

2. **Feature Engineering**  
   - TF-IDF on `productTitle` (top 20 keywords)  
   - Added `title_length` as a new feature

3. **Modeling**  
   - Trained: `LinearRegression`, `RandomForestRegressor`  
   - Evaluation metrics: **Mean Squared Error**, **R² Score**

---

## 📈 Model Results

| Model             | MSE       | R² Score     |
|------------------|-----------|--------------|
| Linear Regression| 177.83    | 0.1075       |
| Random Forest    | 196.19    | 0.0153       |

🔎 **Observation**:  
Even though models were trained successfully, the low R² scores suggest limited predictive power.  
This was likely due to lack of deep features (like ratings, reviews) and skew in the `sold` distribution.

---

## 📁 Project Structure


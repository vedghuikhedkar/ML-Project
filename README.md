# 🛍️ Etsy Product Attribute Prediction using Machine Learning

This repository contains a **Machine Learning project** developed as part of the  
**CA684 – Machine Learning (Spring 2024)** module.

The goal of this project is to predict key attributes of Etsy product listings using
textual and structured data.

---

## 📌 Project Overview

Etsy is a global marketplace with millions of unique product listings.  
Each product includes rich metadata such as title, description, tags, and categorical
attributes.

This project builds machine learning models to **automatically predict multiple product attributes** from this data.

---

## 🎯 Prediction Targets

The models aim to predict the following attributes:

- **Top Category ID**
- **Bottom Category ID**
- **Primary Color ID**
- **Secondary Color ID**

Each task is treated as a **multi-class classification problem** and evaluated using **F1-score**.

---

## 📊 Dataset Description

The dataset (provided by Etsy under NDA) is stored in **Parquet format** and includes:

- Text features: `title`, `description`, `tags`
- Categorical features:  
  `type`, `room`, `craft_type`, `recipient`, `material`, `occasion`,  
  `holiday`, `style`, `shape`, `pattern`
- Image metadata: `image`, `image_width`, `image_height`
- Target labels:  
  `top_category_id`, `bottom_category_id`,  
  `primary_color_id`, `secondary_color_id`

⚠️ **The dataset is confidential and is not included in this repository.**

---

## 🧠 Methodology

1. **Data Preprocessing**
   - Handling missing values
   - Cleaning and normalizing text
   - Encoding categorical features

2. **Feature Engineering**
   - TF-IDF vectorization for text (`title`, `tags`)
   - Structured categorical inputs

3. **Model Training**
   - Multi-class classification models
   - Separate models trained per attribute
   - Evaluation on validation data

4. **Evaluation Metrics**
   - F1-score (weighted & macro)
   - Accuracy
   - Confusion matrix analysis

---

## ⚙️ Technologies Used

- **Python 3**
- **Jupyter Notebook**
- **Pandas** – Data manipulation
- **NumPy** – Numerical operations
- **Scikit-learn** –  
  - TF-IDF Vectorizer  
  - Classification models  
  - F1-score, accuracy, confusion matrix
- **Matplotlib / Seaborn** – Data visualization

---

## 📈 Results (Exact Metrics)

### 🔹 Bottom Category Prediction (Validation Set)

From the classification report generated in the notebook:

- **Accuracy:** `0.22`
- **Weighted F1-score:** `0.14`
- **Macro F1-score:** `0.07`

```text
accuracy                           0.22
macro avg       precision 0.39  recall 0.09  f1-score 0.07
weighted avg    precision 0.39  recall 0.22  f1-score 0.14

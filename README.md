#  Netflix Metadata Classification Pipeline using Random Forest

##  Project Overview
This project is an end-to-end machine learning pipeline built on the Netflix Movies and TV Shows dataset.  
The goal is to predict whether a title is a **Movie** or a **TV Show** using metadata features such as rating, country, and release date information.

---

##  Tech Stack
- **Language:** Python   
- **Data Processing:** Pandas, NumPy  
- **Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn (RandomForestClassifier)

---

##  Workflow

### 1. Data Preprocessing
- Handled missing and malformed date values using safe parsing (`errors='coerce'`)
- Extracted useful time-based features:
  - `year_added`
  - `month_added`
- Cleaned multi-country records by keeping only the primary country

---

### 2. Feature Engineering
- Converted categorical variables into numerical format using **One-Hot Encoding**
- Encoded target variable (`type`) into binary format using LabelEncoder
- Removed unnecessary columns to simplify the dataset

---

### 3. Model Building
- Used **Random Forest Classifier**
- Model configuration:
  - `n_estimators=200`
  - `max_depth=12`
- Applied **stratified train-test split (80/20)** to maintain class balance

---

##  Evaluation Metrics
The model is evaluated using:

- **Accuracy Score** – Overall correctness of predictions  
- **Classification Report** – Precision, Recall, and F1-score  
- **Confusion Matrix** – Breakdown of correct vs incorrect predictions  
- **Feature Importance** – Identifies most influential features  

---

##  How to Run

1. Clone the repository:
```bash
git clone https://github.com/your-repo-name

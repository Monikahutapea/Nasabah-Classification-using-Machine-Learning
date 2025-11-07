# 💳 Customer Classification using Machine Learning

This project focuses on analyzing customer data and building machine learning models to classify customers based on demographic and financial attributes.  
It demonstrates practical applications of data preprocessing, feature engineering, and model evaluation using various classification algorithms.

---

## 📁 Project Overview
The dataset contains information about customers, including their demographics and financial details.  
The main goal is to classify customers based on their characteristics to predict their **Card Category** or customer segment.

---

## 🧩 Objectives
- Perform data cleaning and preprocessing on customer data.
- Handle missing values and outliers for better data quality.
- Encode categorical and scale numerical features.
- Train and compare multiple classification models.
- Evaluate and determine the best-performing algorithm.

---

## 🛠️ Tools & Libraries
- **Python 3.8+**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**, **Missingno**
- **Scikit-learn**
- **XGBoost**, **LightGBM**

---

## ⚙️ Workflow
1. **Data Preprocessing**
   - Load dataset (`data_nasabah.csv`)
   - Handle missing values using `SimpleImputer`
   - Treat outliers using visual analysis (Boxplot & Histogram)
   - Encode categorical features using `OrdinalEncoder` or `OneHotEncoder`
   - Scale numerical features with `StandardScaler` or `MinMaxScaler`

2. **Exploratory Data Analysis (EDA)**
   - Analyze feature distributions and correlations
   - Visualize categorical and numerical variables
   - Identify key customer segments

3. **Model Building**
   - Implement and compare multiple classification models:
     - Logistic Regression  
     - Random Forest Classifier  
     - K-Nearest Neighbors (KNN)  
     - Support Vector Machine (SVM)  
     - Naive Bayes  
     - XGBoost  
     - LightGBM
   - Use `GridSearchCV` for hyperparameter tuning

4. **Feature Selection**
   - Apply Recursive Feature Elimination (RFE) to select the most influential features.

5. **Model Evaluation**
   - Evaluate models using:
     - Accuracy Score  
     - Confusion Matrix  
     - Classification Report  
   - Compare performance across different algorithms.

---

## 📈 Results
- Successfully cleaned and prepared customer dataset.
- Built and evaluated multiple classification models.
- Determined the most accurate model for customer card category prediction.
- Visual insights and model comparisons provided a deeper understanding of key customer characteristics.

---

## 💡 Key Insights
- Certain demographic and financial factors strongly influence card type classification.  
- Feature selection significantly improves model performance.  
- Ensemble models like XGBoost and LightGBM tend to achieve higher accuracy compared to traditional algorithms.

---

## 📂 Project Structure

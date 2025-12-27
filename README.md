# 🏥 Patient Risk Stratification Using PCA and K-Means Clustering

## 📌 Overview
This project applies **unsupervised learning** techniques to multivariate patient vital data to identify hidden physiological patterns and stratify patients into meaningful subgroups.  
Principal Component Analysis (PCA) is implemented **from scratch** using linear algebra, followed by **K-Means clustering** on the reduced feature space.

The project demonstrates how dimensionality reduction and clustering can support **data-driven decision-making in healthcare** without relying on predefined labels.

---

## 📊 Dataset Description
The dataset contains patient vital signs commonly used in clinical monitoring:

- Heart Rate  
- Systolic Blood Pressure  
- Diastolic Blood Pressure  
- Mean Arterial Pressure  
- Respiratory Rate  
- Oxygen Saturation  
- Body Temperature  
- Body Mass Index (BMI)  
- Age  

Additional columns:
- **Gender**
- **Risk_Category**

⚠️ *Gender and Risk_Category are NOT used during clustering and are only used for post-clustering interpretation.*

---

## 🎯 Objective
To reduce correlated medical variables using PCA and apply K-Means clustering to identify clinically meaningful patient subgroups based on physiological similarity.

---

## 🔍 Exploratory Data Analysis
- Examined feature distributions and normality
- Observed strong correlations among:
  - Blood pressure variables
  - Heart rate and cardiovascular indicators
  - Respiratory rate and oxygen saturation

Due to multicollinearity, direct clustering in the original feature space was avoided.

---

## ⚙️ Methodology

### 1️⃣ Principal Component Analysis (From Scratch)
Steps followed:
- Mean centering and standardization
- Covariance matrix computation
- Eigenvalue and eigenvector decomposition
- Sorting eigenvalues in descending order
- Projection onto principal components

**Results:**
- First 3 principal components explain ~**91%** of total variance

**Interpretation:**
- **PC1:** Cardiovascular system (BP, Heart Rate)
- **PC2:** Metabolic & age-related factors (BMI, Age, Temperature)
- **PC3:** Respiratory system (Respiratory Rate, Oxygen Saturation)

---

### 2️⃣ K-Means Clustering
- Applied on PCA-transformed data
- Optimal number of clusters selected using the **Elbow Method**
- No clinical labels used during clustering

---

## 📈 Visualization
- 3D PCA scatter plots before clustering
- 3D PCA plots colored by K-Means clusters
- Interactive Plotly visualizations
- Risk category and gender used only for interpretation

---

## 🧠 Key Findings
- PCA effectively reduced dimensionality while preserving physiological meaning
- K-Means identified distinct patient phenotypes
- Clusters showed clear separation in PCA space
- Certain clusters aligned with higher clinical risk during post-analysis

---

## 🏥 Medical Significance
This approach can be applied to:
- Patient stratification and triage
- Early risk identification
- Exploratory healthcare analytics
- Clinical decision support systems

It is especially useful when labeled medical data is limited or unavailable.

---

## 🛠️ Tools & Technologies
- Python
- NumPy
- Pandas
- Matplotlib
- Plotly
- Scikit-learn (for K-Means only)


---

## ✅ Conclusion
This project demonstrates how PCA combined with K-Means clustering can uncover hidden structures in patient vital data, reduce complexity, and support data-driven healthcare insights using unsupervised learning.

---

## 👩‍💻 Author
**Sneha Vishwakarma**  


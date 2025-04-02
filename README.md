# Lead Scoring Model for X Education  

## Introduction  

X Education is an online course provider targeting industry professionals. The company generates leads through various channels, including website visits, form submissions, and referrals. However, the current lead conversion rate is only around 30%, indicating inefficiencies in identifying high-potential leads.  

This project aims to build a **lead scoring model** that predicts the likelihood of a lead converting into a paying customer. By prioritizing "Hot Leads," the sales team can focus efforts on prospects with the highest conversion potential, improving efficiency and revenue.  

## Objective  

The primary goal is to:  
- **Analyze** historical lead data to identify patterns.  
- **Build** a predictive model to score leads based on conversion probability.  
- **Optimize** sales efforts by targeting high-scoring leads.  

Key questions addressed:  
- What factors influence lead conversion the most?  
- How can the model improve the current 30% conversion rate?  

## Steps Conducted  

1. **Data Cleaning & Preprocessing**  
   - Removed columns with >50% missing values (e.g., "Lead Profile").  
   - Imputed missing categorical values with "Other" categories.  
   - Capped outliers in numerical features (e.g., "TotalVisits").  
   - Dropped skewed variables (e.g., "Do Not Call").  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized lead sources, occupations, and geographic trends.  
   - Identified strong correlations (e.g., "Total Time Spent on Website" vs. conversion).  

3. **Feature Engineering**  
   - Created dummy variables for categorical features.  
   - Selected top 20 features using **Recursive Feature Elimination (RFE)**.  

4. **Model Building**  
   - Trained a **logistic regression model** with iterative refinement.  
   - Evaluated performance using accuracy, precision, recall, and ROC-AUC.  

5. **Model Evaluation**  
   - **Accuracy**: 81.6%  
   - **Sensitivity (Recall)**: 69.2%  
   - **Specificity**: 89.2%  
   - **ROC-AUC**: 0.88  

6. **Optimal Cutoff Selection**  
   - Balanced sensitivity and specificity at a **0.5 probability threshold**.  

## Results  

- **Top Predictors of Conversion**:  
  - ✅ **Total Time Spent on Website** (strong positive correlation).  
  - ✅ **Working Professional** (high conversion rate).  
  - ✅ **Lead Source: Google/Direct Traffic** (most productive channels).  
- **Model Performance**:  
  - The model achieves **81.6% accuracy** and an **AUC of 0.88**, indicating strong predictive power.  

## Conclusion  

The lead scoring model successfully identifies high-potential leads, enabling X Education to:  
- **Increase conversion rates** by focusing on "Hot Leads."  
- **Optimize marketing spend** by prioritizing high-performing channels (e.g., Google Ads).  
- **Improve sales efficiency** by reducing time spent on low-probability leads.  

Future improvements could include testing **ensemble models (Random Forest, XGBoost)** and incorporating real-time behavioral data.  

---

Feel free to explore the code, tweak the model, and visualize the results further. Contributions and feedback are welcome!  

**Tools Used:**  
- Python (Pandas, NumPy, Scikit-learn, StatsModels)  
- Matplotlib, Seaborn (Visualization)  
- Jupyter Notebook  

**Author:** Jay Thakur

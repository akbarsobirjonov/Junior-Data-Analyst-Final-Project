🏁 **Junior Data Analyst Final Project**

📌 **Project Summary**

This is my capstone project for the Junior Data Analyst course. I worked with anonymized customer data from a sporting goods retailer to solve real-world business problems using data analysis and machine learning.

🔍 **Objectives:**

- Clean and prepare raw data for analysis
- Rebuild missing gender information using classification
- Evaluate the success of a past marketing campaign using A/B testing
- Segment customers with clustering
- Predict purchase interest using a machine learning model

📦 **Data Sources**

**The dataset includes:**

1. shop_database.db with:

    - personal_data: client demographics 
    - personal_data_coeffs: calculated client metrics (e.g. personal_coef)
    - purchases: product details, discounts, prices, etc.

2. Extra files:
    - personal_data.csv.gz: demographic records with missing gender
    - ids_first_company_positive.txt: users who received a personalized discount
    - ids_first_company_negative.txt: control group for A/B testing

**📌 Note: Only users from country code 32 were included in the analysis.**

🧠 **Project Breakdown**

**1.** 📊 **Data Preprocessing**
- Filtered records by country
- Merged external data to fill in missing client info
- Cleaned and normalized product names and colors
- Handled missing values (e.g. filled missing ages with median)
- Engineered useful features: numeric dates, discount flag, etc.

**2.** 🚻 **Gender Classification**

**To fill in missing gender values:**
- Trained a RandomForestClassifier on complete records
- Encoded categorical variables
- Achieved AUC ROC > 0.85
- Predicted gender for incomplete entries with high accuracy

**3. 📈 A/B Testing (Email Campaign)**

Evaluated the first marketing campaign using test and control groups:

- Group A: 5,000 users received a personal discount email
- Group B: similar users without the discount

**Key results:**

- Calculated conversion rates for both groups
- Conducted Z-test for statistical significance
- p-value < 0.05 → Campaign was effective

**✅ Recommendation: Use more personalized campaigns like this in the future.**

**4. 👥 Customer Segmentation (Clustering)**

**Used KMeans to group users based on behavior:**
- Selected features: age, personal_coef, activity, preferences
- Determined 4 optimal clusters
- Identified traits of each cluster (e.g. high spenders, discount seekers)

**📢 Insight:**
- Segment-based targeting can improve campaign results
- Premium customers (Cluster 2) = high ROI
- Inactive users (Cluster 3) = potential re-engagement target

**5. 🛍 Purchase Propensity Model**

**Built a predictive model for clients in city 1188, country 32:**
- Trained an XGBoostClassifier
- Used client profile + product info + past behavior
- AUC ROC > 0.80

**Key features:**
discount, gender, age, personal_coef, product category

**🎯 Recommendation: Use this model to optimize future campaigns and reduce marketing costs.**

**📚 Tools & Technologies**
- Python: pandas, scikit-learn, xgboost, matplotlib, seaborn
- SQL (SQLite)
- Jupyter Notebook
- A/B Testing (Z-test)
- ML Models: Random Forest, XGBoost, KMeans

🙋‍♂️ Author
Akbar Sobirjonov
Final Project | Junior Data Analyst Course
Platform: Skillbox

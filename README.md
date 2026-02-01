## **Predictive Modeling of Banking Customer Attrition using Ensemble Learning and Gradient Boosting**

### **Project Overview**

This project addresses the critical challenge of customer attrition within the retail banking sector. By analyzing historical customer data, I developed a machine learning framework to identify high-risk churners, enabling the bank to deploy proactive retention strategies. Using a comparative modeling approach that included **XGBoost** and **LightGBM**, the project successfully classified at-risk profiles with optimized performance across multiple classification metrics, providing a scalable solution for maintaining market share.

### **Business Understanding**

The primary stakeholders are bank executives and customer relationship management (CRM) teams tasked with reducing "churn"—the rate at which customers terminate their relationship with the institution. In the competitive 2026 banking landscape, retaining an existing customer is estimated to be **five to seven times more cost-effective** than acquiring a new one (Kumar & Petersen, 2012). Research indicates that even a **5% increase in customer retention** can lead to a profit increase of **25% to 95%** (Reichheld & Sasser, 1990; Tran et al., 2023). The business problem focuses on shifting from reactive service recovery to predictive intervention, identifying dissatisfaction before a customer exits the ecosystem.

### **Data Understanding**

The analysis was performed on a comprehensive banking dataset featuring demographic and financial indicators.

* **Data Scope:** Features included credit scores, geography, gender, age, tenure, account balance, number of products utilized, and active membership status.
* **Timeframe:** The dataset captures long-term behavioral patterns to distinguish between temporary inactivity and true churn.
* **Limitations:** A key limitation identified was **class imbalance**, where churners represented a minority of the total population—a common trait in banking data that requires specific sampling techniques to prevent model bias.
* **Exploratory Data Analysis (EDA):** Visualizations were created to map the correlation between variables (such as age and balance) and the target variable to isolate the most significant churn drivers.

### **Modeling and Evaluation**

To ensure a robust fit, I implemented and optimized a diverse range of supervised learning algorithms using **GridSearchCV** and **k-fold cross-validation**:

* **Models Evaluated:** Logistic Regression, Random Forest Classifier, Gradient Boosting Classifier, XGBoost (XG Boosting), Light Gradient Boosting Machine (LightGBM), and Ensemble Learning Algorithms.
* **Evaluation Metrics:** To select the superior classifier, performance was benchmarked against four critical metrics:
* **Accuracy:** Overall correctness of the model.
* **Precision:** The ability to minimize false "churn" alarms.
* **Recall:** The ability to capture the maximum number of actual churners (crucial for retention).
* **ROC-AUC:** The aggregate measure of performance across all possible classification thresholds.

### **Conclusion**

The results demonstrate that gradient boosting methods (XGBoost/LightGBM) offer the most effective balance of precision and recall for banking churn. I recommend that the stakeholder integrate these predictive insights into their CRM systems to trigger **automated, personalized retention offers** (e.g., fee waivers or tailored financial products) when a customer’s "churn probability" exceeds a defined threshold.

**Future Steps:**

* **Dynamic Feature Integration:** Incorporate real-time transaction frequency and mobile app login data to capture sudden shifts in customer engagement.
* **Model Interpretability:** Implement SHAP (Shapley Additive Explanations) values to provide branch managers with specific reasons *why* an individual customer is flagged, allowing for more empathetic human intervention.

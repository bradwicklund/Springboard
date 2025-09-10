# Customer Segmentation and Satisfaction Prediction in Olist E-Commerce  

## 0. Data  
Using the [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), we set out with the goal of analyzing customer behavior and predicting satisfaction. The dataset contains over 100,000 orders placed between 2016 and 2018 across multiple marketplaces in Brazil. Data include information on customers, orders, products, payments, reviews, sellers, and geolocation.  

## 1. Problem Identification  
The problem we set out to solve was whether Olist’s transactional and review data could be used to both segment customers and predict satisfaction. Rather than relying on broad, undifferentiated strategies, Olist could use clustering to identify loyal, at-risk, and one-time buyers, and regression modeling to uncover the operational factors most strongly tied to customer satisfaction. These insights could guide retention campaigns, delivery improvements, and payment optimizations that directly reduce churn and increase lifetime value.  

## 2. Data Cleaning and Wrangling  
During data cleaning and wrangling, multiple relational tables (customers, orders, order_items, payments, reviews, sellers, products, product category translations, and geolocation) were merged into an integrated analytical dataset. Timestamps were converted into datetime objects, missing values in critical fields (e.g., delivery dates, review scores) were dropped, and implausible outliers such as negative delivery times were removed.  

[Notebook: Data Wrangling](https://github.com/bradwicklund/Springboard/blob/main/Capstones/olist_analysis/notebooks/01.data_wrangling.ipynb)  

## 3. EDA  
Exploratory analysis revealed several key trends. Review scores were heavily skewed toward 5 stars, but late deliveries were strongly associated with lower ratings. Credit cards dominated payments, while boleto and voucher payments were linked to slightly lower satisfaction. RFM analysis showed that most customers were one-time buyers, while a small minority contributed disproportionately to revenue.  

[Notebook: EDA](https://github.com/bradwicklund/Springboard/blob/main/Capstones/olist_analysis/notebooks/02.EDA.ipynb)  

## 4. Preprocessing and Feature Engineering  
Features were engineered to capture behavioral and operational dimensions. Delivery delay was calculated as the difference between estimated and actual delivery dates. Order value combined product prices and freight charges. Payment types were one-hot encoded. At the customer level, Recency, Frequency, and Monetary (RFM) scores were created. Continuous features were standardized to prepare the data for clustering and regression modeling.  

[Notebook: Preprocessing & Feature Engineering](https://github.com/bradwicklund/Springboard/blob/main/Capstones/olist_analysis/notebooks/03.preprocessing_modeling.ipynb)  

## 5. Modeling  
Two modeling tracks were pursued:  
- **Unsupervised Clustering:** K-Means clustering on RFM scores identified four customer segments, ranging from high-value loyal buyers to one-time low-value purchasers.  
- **Supervised Regression:** Linear Regression, Random Forest Regressor, and Gradient Boosting Regressor were tested to predict review scores. Gradient Boosting achieved the best balance of R² and RMSE, while feature importance confirmed that delivery delay was the strongest predictor of dissatisfaction.  

[Notebook: Modeling](https://github.com/bradwicklund/Springboard/blob/main/Capstones/olist_analysis/notebooks/03.preprocessing_modeling.ipynb)  
[Model Metrics](https://github.com/bradwicklund/Springboard/blob/main/Capstones/olist_analysis/models/model_metrics.rtf)

## 6. Reports  
Final reports include the PDF report and presentation slides summarizing the analysis, models, and recommendations.  

[Reports Folder](https://github.com/bradwicklund/Springboard/tree/main/Capstones/olist_analysis/reports)  
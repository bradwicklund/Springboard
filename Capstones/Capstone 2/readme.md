# Segmenting Shopper Sessions: A Clustering Approach to E-Commerce Behavior

## 0. Data
Using clickstream data provided by UC Irvine Machine Learning Repository, we set out with the goal of analyzing the data and segmenting the customer base in to clusters for the purpose of future targeted online marketing campaigns.  The dataset contains information on clickstream from online store offering clothing for pregnant women. Data are from five months of 2008 and include, among others, product category, location of the photo on the page, country of origin of the IP address and product price in US dollars.

https://archive.ics.uci.edu/dataset/553/clickstream+data+for+online+shopping

## 1. Problem Identification
The problem we set out to solve was if our online shopping data could be separated into useful clusters for the purpose of creating targeted marketing campaigns.  Given the availabilty of the shopping data, rather than posting new products with no clear strategy on how to sell the products, the goal is to provide actionable insights so that when new items are posted to the website they can be marketed to the cluster most likely to buy and so that timed sales can also be advertised to the cluster most likely to buy them.

## 2. Data Cleaning and Wrangling
During data cleaning and wrangling no missing values were found and it was determined that most of our features were categorical, rather than numercial, and would need to be encoded prior to creating a clustering model.  It was also determined that 80% of sales are from customers in Poland, where the website is based.  Another 10% are from the Czech Republic and the final 10% are from all remaining countries and regions.  

https://github.com/bradwicklund/Springboard/blob/main/Capstones/Capstone%202/notebooks/18.6%20-%20Capstone%202%20-%20Data%20Wrangling.ipynb

## 3. EDA
Based on the exploration of data, some relationships emerged. It appears that when an item is displayed on the first page is it more likely to be purchased. It also appears that when an item appears in the top middle and top left of a page it is more likely to be purchased.

Another observed trend is that items that are olive, red, blue, pink, and black have an average price that is higher than the overall mean price of $43.80.

We also observed that there are 1,923 items with the outlier price of $82.00.

https://github.com/bradwicklund/Springboard/blob/main/Capstones/Capstone%202/notebooks/22.5%20-%20Capstone%202%20-%20EDA.ipynb

## 4. Preprocessing and Data Training Development
Given that most of our features are categorical variables, it was critical that during our preprocessing step we created dummy variables.  During this phase of the project we also standardized the data.

https://github.com/bradwicklund/Springboard/blob/main/Capstones/Capstone%202/notebooks/27.3%20-%20Capstone%202%20-%20Preprocessing%20and%20Training%20Data%20Development.ipynb

## 5. Modeling
We tested our data with three unsupervised clustering models: KMeans, Hierarchichal Clustering, and DBSCAN

https://github.com/bradwicklund/Springboard/blob/main/Capstones/Capstone%202/notebooks/28.3%20-%20Capstone%202%20-%20Modeling.ipynb

## 6. Reports
Final reports of findings including PDF and PPT.

https://github.com/bradwicklund/Springboard/tree/main/Capstones/Capstone%202/reports
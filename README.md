# Customer-segmentation   
#### Poonam Solanke
---
## Introduction

This report presents an analysis of sales data using the online retail dataset. The dataset includes information on invoices, customer details, product descriptions, quantities, unit prices, and countries. The analysis aims to gain insights into customer behavior and segment customers based on their purchasing patterns.

### Data Overview

•	Total number of unique invoices: 2048
•	Total number of unique customers: 166


### RFM Analysis

RFM (Recency, Frequency, Monetary) analysis is performed to segment customers based on their purchasing behavior. The following RFM scores are assigned to each customer:

- LastGroup (Recency): This represents the grouping of customers based on the number of days since their last purchase. Customers who have made a recent purchase are assigned lower group numbers, indicating their higher engagement or likelihood of making repeat purchases.

- VolumeGroup (Frequency): This represents the grouping of customers based on the frequency of their purchases. Customers who have made a higher number of purchases are assigned lower group numbers, indicating their higher frequency of engagement or loyalty.

- AvgGroup (Monetary Value): This represents the grouping of customers based on their average purchase amounts. Customers with higher average purchase amounts are assigned lower group numbers, indicating their higher value or spending potential. 

The SQL code creates an RFM (Recency, Frequency, Monetary) model using customer sales data. RFM analysis is a technique used in marketing and customer relationship management to segment customers based on their buying behavior.

The SQL code performs the following steps:
- Extracts relevant data from the "sales" table, including the invoice number, invoice date, customer ID, country, quantity, unit price, and calculates the total amount for each invoice.
- Generates summary tables that provide the total amount and average amount spent by each customer, the number of days since their last purchase, and the frequency of their purchases.
- Assigns RFM scores to each customer by dividing them into quintiles (groups of equal size) based on average spending, recency, and frequency.
- Provides frequency tables showing the size of each group within the RFM scores.
- Creates a new table called "rfmModel" that contains all the calculated RFM metrics for each customer.

The RFM model helps segment customers into different groups based on their purchase behavior, allowing businesses to target specific customer segments with tailored marketing strategies. It provides insights into which customers are the most valuable, which ones are at risk of churning, and identifies opportunities for cross-selling and upselling.


### Data Exploration 

![](https://github.com/poonam-solanke/customer-segmentation/blob/main/images/Dashboard.png)
![](https://github.com/poonam-solanke/customer-segmentation/blob/main/images/Clustering.png)
![](https://github.com/poonam-solanke/customer-segmentation/blob/main/images/CustomerSegments.png)
![](https://github.com/poonam-solanke/customer-segmentation/blob/main/images/RFMScoreBarGraph.png)
![](https://github.com/poonam-solanke/customer-segmentation/blob/main/images/SpendByCountries.png)

### Conclusion
1.	Geographic Segmentation: The dataset includes customers from various countries, such as the United Kingdom, Germany, Portugal, Spain, and Belgium. This indicates that the company has an international customer base.
2.	Customer Value: The "CustomerTotal" column represents the total amount spent by each customer. The range varies from relatively low values to significantly higher amounts. This suggests the presence of both low-value and high-value customers within the dataset.
3.	Customer Engagement: The "DaysSinceLast" column indicates the number of days since the last purchase made by each customer. There is a wide range of values, indicating different levels of customer engagement. Some customers have made recent purchases, while others have not made any purchases for a considerable amount of time.
4.	RFM Score: The "RFM Score" column represents the combined RFM (Recency, Frequency, Monetary) score for each customer. This score is commonly used in customer segmentation analysis. Higher RFM scores generally indicate more valuable and engaged customers, while lower scores may suggest customers who are less active or less valuable.
5.	Customer Segments: The "Segments" column categorizes customers into different segments based on their RFM scores. The provided segments include "Potential Loyalist," "At Risk," and "Lost," among others. These segments help identify different customer groups and guide targeted marketing strategies and retention efforts.
6.	Potential Loyalist Opportunities: The presence of customers in the "Potential Loyalist" segment suggests an opportunity for the company to engage and nurture these customers further. They have shown potential for loyalty based on their RFM scores and could be targeted with personalized offers or loyalty programs to encourage repeat purchases and strengthen their relationship with the brand.
7.	At-Risk Customers: The "At Risk" segment includes customers who have shown signs of decreased engagement or activity. Proactive measures can be taken to prevent these customers from becoming "Lost" customers. Targeted communications, re-engagement campaigns, or special offers may help retain their loyalty.
8.	Lost Customers: The "Lost" segment represents customers who haven't made a purchase for a significant period or have disengaged completely. While it may be challenging to re-engage these customers, a targeted win-back strategy could be implemented to regain their trust and bring them back to the brand.
9.	Volume and Average Groupings: The dataset includes columns like "CustomerVolume," "AvgGroup," and "VolumeGroup." These groupings provide insights into customer behavior patterns and can be used to identify trends or differences among customer groups based on their purchase volume and average spending.

These insights provide a foundation for further analysis and decision-making. They can be used to refine marketing strategies, tailor customer communication, identify high-value customers, and develop personalized approaches for different customer segments.



### Tools

- **MySQL**
- **Tableau**
- **Excel**

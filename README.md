# Instacart Grocery Basket Analysis Project
**Purpose and Context:** Instacart is an online grocery store that operates via an app. This project focused on analyzing Instacart's sales patterns and conducting exploratory data analysis to better segment customer profiles. Our goal is to understand the diverse customers in their database and their purchasing behaviors.

### Project Goals:
- Determine busiest hours and days of the week.
- Identify departments that more popular than others.
- Classify customers based on their behaviour.


## Tools and Techniques
For this analysis, I utilize Python as my primary tool for analysis and for data visualization. Leveraging the power of Python, I employ various libraries including:
* NumPy for numerical computations
* Pandas for data manipulation and analysis
* Seaborn and Matplotlib for data visualization

Additionally, the following techniques were used throughout the project:
* Data wrangling
* Data merging
* Deriving new variables
* Data Cleaning
* Aggregating Data
* Creating Population Flows (Excel)




Further, the following techniques are employed throughout the analysis:
* Data Cleaning and summarizing
* Data Wrangling
* Data Merging
* Deriving New Features
* Population Flows
* Creating Customer Profiles


## Datasets 
I used an  open-source data sets from Instacart. All the sales data we have is only for year 2017. Hence, we must keep in the relevance of this analysis before interpreting the results. 
You can click on this link to access the dataset. 
* [Instacart Dataset] (https://gist.github.com/jeremystan/c3b39d947d9b88b3ccff3147dbcf6c6b)
I prepared the datasets given following a series of steps. The steps are as listed here.
1. Explored shape of the data frames, data types of the columns, and summary statistics of the numerical columns
2. Performed data wrangling by renaming columns, dropping columns, changing data types of columns
3. Created Data Profiles for Raw Data
4. Checked data for consistency addressing mixed data types, handling duplicates, and missing data
5. Merged data frames for analysis and derived new variables



### Challenges
All the sales data we have is only for year 2017. Hence, we must keep in the relevance of this analysis before interpreting the results. I resolved the below listed problems with the dataset:
* Some of the products information was missing. I removed this missing data as it constituted less than 5% of the total data points.
* Removed first_name and last_name from the dataset for security reasons and they were not needed for the analysis.
* The missing values for days_since_prior order was retained as for the first order of a customer days since prior order will be NA.

Apart from the challenges with the dataset, creating customer profiles using the data was difficult. The most challenging part was to decide which features to keep and which features should be dropped while creating customer profiles as there were a number of possibilities for customer profiles. 

Note: I am interested recreating the customer profiles using machine learning algorithms such as clustering to create more reliable customer profiles. Updates regarding which will be posted here.


## Key Questions
Although there are many questions one can ask, the following questions dictated the direction of the analysis I have presented here.

1. What are the busiest days and hours for order placement?
2. How does the time of day influence customer spending behavior?
3. Can we simplify product price range groupings for targeted marketing?
4. Which product categories are most popular among Instacart customers?
5. What is the distribution of brand loyalty among users?
6. Are there differences in ordering habits based on customer loyalty status?
7. How do ordering habits vary across different regions?
8. Is there a relationship between age, family status, and ordering behavior?
9. What demographic classifications emerge from the data?
10. How do different customer profiles differ in terms of order price, frequency, and product preferences?

## Understanding Sales Trend
I started with identifying busiest days of the week and busiest hours of the day as was asked by our sales department. I also looked at average prices per order over 24 hours. 
<p align = "center">
<img alt = "light" src = "https://github.com/user-attachments/assets/f0a0ec2b-711f-4cd4-a487-d263910a969b" width = "80%">
</p>
The days are encoded as Saturda(0), Sunday(1), Monday(2), Tuesday(3), Wednesday(4), Thursday(5), and Friday(6).

<p align="center">
  <img alt="Light" src="https://github.com/user-attachments/assets/7cacffd6-d22f-4a5c-b5ce-849716ade9a2" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Dark" src="https://github.com/user-attachments/assets/d6714e53-9291-47a3-b5a8-c3f4b6bd5688" width="45%">
</p>

- We found that Saturday and Sunday were the busiest days of the week and Wednesday was the least busy day of the week.
- The busiest hours of the day were between 10 AM and 3 PM and least busy hours were between 12 AM and 3 AM.
- Average price paid is highest around 3 AM and least around 10 AM. The prices fluctuate throughout the day.

After reviewing the sales pattern over time, I turned my attention towards sales by department and pricing distribution of all the items to better segment the products. 
<p align="center">
  <img alt="Light" src="https://github.com/user-attachments/assets/6b7d6c72-95a0-4fcb-8d0e-95f89ccae624" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Dark" src="https://github.com/user-attachments/assets/ae82a382-67b6-4da4-a6b7-fe20080f344d" width="45%">
</p>
We identified departments with the most orders and found that produce department had the most orders and this was followed by dairy eggs, snacks, and beverages departments. The least popular departments in terms of total orders were bulk, other, missing, pets, and alcohol.
Most of the orders have priced less than $15. Only a few orders in comparison are priced more than $15. This gave me an idea about how the segmentation can be done.








# Results
Following in an excerpt from the results of the analysis to give you an overview of the resutls. For complete results please read read the Report. [Link to the final Report](https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/commit/f10d4b9d9eb6ec4d7dd1d17135068f5238ecc2b8)

One of the questions were to find the busiest days and hours of the week. 

<p align="center">
  <img alt="Light" src="https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/assets/153047871/f21610e5-d4b0-4c1b-b244-fd367169ddff" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Dark" src="https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/assets/153047871/cbf6ec0e-a30e-4fe0-b663-8f23b7f43b5b" width="45%">
</p>
Labelling: 0 (Saturday), 1 (Sunday), 2 (Monday), 3 (Tuesday), 4 (Wednesday), 5 (Thursday), and 6 (Friday).

* Tuesday and Wednesday have recorded fewest total orders and on these days ads should be scheduled.
* Saturday and Sunday have seen maximum number of total orders.
* The orders start to increase when weekend is approaching and start to decline when weekdays begin.

In the analysis, we also found the distribution of customers based on loyalty type and income brackets. Most of the ordes were placed by regular customers. Surprisingly, loyal customer placed less number of total orders than regular customers. This is due to higher number of regular customers.

<p align="center">
<img width="45%" alt="image" src="https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/assets/153047871/18646135-f080-4085-9f1f-014cc2ff80ce">
&nbsp; &nbsp; &nbsp; &nbsp;
<img width="45%" alt="image" src="https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/assets/153047871/0abd31e1-3c1e-49bb-a28b-94222b1c285f">
</p>
Most of the customers belong to Medium Income group or High Income group. The Low Income category had the least number of customers.
For a more comprehensive report I urge you to download the final report file.

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

Further, the following techniques were employed throughout the analysis:
* Data Cleaning and summarizing
* Data Wrangling
* Data Merging
* Deriving New Features
* Population Flows
* Creating Customer Profiles


## Datasets 
I used an  open-source data sets from Instacart. All the sales data we have is only for year 2017. Hence, we must keep in the relevance of this analysis before interpreting the results. 
You can click on this link to access the dataset. 
* [Instacart Dataset](https://gist.github.com/jeremystan/c3b39d947d9b88b3ccff3147dbcf6c6b)
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
  <img alt="Light" src="https://github.com/user-attachments/assets/6b7d6c72-95a0-4fcb-8d0e-95f89ccae624" width="80%">
</p>
We identified departments with the most orders and found that produce department had the most orders and this was followed by dairy eggs, snacks, and beverages departments. The least popular departments in terms of total orders were bulk, other, missing, pets, and alcohol.
<p align="center">
  <img alt="Dark" src="https://github.com/user-attachments/assets/ae82a382-67b6-4da4-a6b7-fe20080f344d" width="80%">
</p>
Most of the orders have priced less than $15. Only a few orders in comparison are priced more than $15. This gave me an idea about how the segmentation can be done.

## Profiling Customers
After developing an understanding of the sales trend, I looked at our customer data to find key features and create profiles based on them.
<p align="center">
  <img alt="Light" src="https://github.com/user-attachments/assets/5998d5e4-d7d0-43de-91ce-941ac103f5a7" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Dark" src="https://github.com/user-attachments/assets/e0323565-b694-4cc0-adaa-cdbbc45f7758" width="45%">
</p>

- Number of dependents fluctuates as age increases. There is no clear relationship between the two variables.
- There isn't a clear relationship between age and income as evident from this scatter plot. However, extremely high salaries are recorded for individuals with age more than 40 years.

These results led me to look in a different direction. So, I decided to look at the create profile customer using their ordering frequency and family size.

<p align="center">
  <img alt="Light" src="https://github.com/user-attachments/assets/e350f6af-236c-43f1-984e-987d324c713e" width="45%">
  &nbsp; &nbsp; &nbsp; &nbsp;
   <img alt="Light" src="https://github.com/user-attachments/assets/07c41744-0db5-476a-a46c-baf7da1b6ed9" width="45%">
</p>

- A loyal customer was someone with more than 40 orders whereas a new customer was someone with less than 10 orders.
- Most of the orders were placed by regular customers.
- Surprisingly, loyal customer placed lesser number of total orders than regular customers. This is due to higher number of regular customers.
- All the households have approximately the same number of customers. This distribution depends on the way we define household.

I also considered income, prefered time of ordering and age to create customer profiles. Following were my observations:
<p align="center">
  <img alt="Light" src="https://github.com/user-attachments/assets/b70473e1-abe7-45fa-bf50-bca6d1182c84" width="45%">
  &nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Dark" src="https://github.com/user-attachments/assets/e5281cab-20ec-42c9-af8e-429576104268" width="45%">
  &nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Dark" src="https://github.com/user-attachments/assets/150b7acc-67a7-47f0-ae3d-5cb939ce0aee" width="40%">
</p>

- Most of the customers belong to Medium Income group or High-Income group.
- The Low-Income category had the least number of customers.
- Most of the customers are daytime shoppers, ordering between 11 AM and 5 PM.
- The least number of shoppers are Night Owls, ordering between 11 PM and 5 AM.
- Majority of customers are Senior adults, having age more than 55 years.
- The age group with least number of users is Young Adult.

Using the derived variables, I checked at the distribution of profiles and found that there are several possibilities. I observed that, in all the four regions the behavior of groups by prefered time of day was same across the regions. Early birds, placed higher orders per user than all the other categories. Those ordering at night placed least number of orders per user in all regions. In this case, the difference between the categories was more noticeable.
<p align = "center"> 
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/2d724ddf-c5a1-46dc-83fa-288cb2d7733e">
</p>

Moreover, the distribution of total orders was same as noticed earlier. In all the departments, most of the orders were placed by senior adults. Young adults placed least number of total orders in all departments.
<p align = "center">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/17747a0b-8ac2-479f-8d50-b4db47a92884">
</p>

When I looked at the relationship between brand loyalty, customer types, and total orders I discovered the following:
<p align ="center">
  <img width="45%" alt="image" src="https://github.com/user-attachments/assets/68bd5e12-43c6-4596-af4d-23f35e4bd38f">
</p>

- When we compare brand loyalty and ordering habits, for all the 4 types of customers, regular customer placed most orders, followed by loyal customers followed by new customers.
- This pattern was consistent with what we have observed earlier.
- Maximum orders were placed by regular and daytime shoppers. Minimum number of orders were placed by New and Loyal customers who were Night Owls.

Finally, I looked at the relationship between brand loyalty, regions, and orders and found the following:
<p align ="center">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/4b167850-2651-4dd4-8751-a2ebfb478d6c">
</p>

- Maximum orders were placed by regular customers from South region.
- Minimum orders were placed by New customers in Northeast region.
- The distribution of brand loyalty was same in all 4 regions.

## Conclusion and Recommendations

Based on the findings during the analysis I produced the following recommendations:
1. We can advertise more during the middle of the week, on Wednesday and during night for those who order at night to increase sales.
2. We can focus more on departments with lower number of orders such as bulk, other, pets, and alcohol by giving special offers and doing targeted advertisements.
3. When it comes to ordering habits, customers regardless of them brand loyalty exhibit similar behavior. For all the loyalty status, maximum customers order during daytime.
4. The average sales price was least in the early morning and therefore, we can advertise more in the early morning.

**What could I do better?**
I would have created different salary segmentation for creating customer profiles. Further, I could have selected different features with higher variations to create different customer profiles. Creating customer profiles is very complex and selecting the right feature is of paramount importance while doing this.

Following in an excerpt from the results of the analysis to give you an overview of the resutls. For more details about criterion for deciding features look at my report in Excel sheet. [Link to the final Report](https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/commit/f10d4b9d9eb6ec4d7dd1d17135068f5238ecc2b8)

Do you have any questions or suggestions for me? Feel free to reach out via my [LinkedIn](https://www.linkedin.com/in/nirav-bariya/) profile or [email](mailto:nkb.bariya@gmail.com) me. Thank you for your time. I hope you found something useful. Have a great rest of day! 

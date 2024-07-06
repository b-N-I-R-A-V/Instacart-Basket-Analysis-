# Instacart Grocery Basket Analysis Project
In this project, we are analyzing Instacart's Grocery Basket who wants to uncover more information about their sales pattern. The instacart stakeholders are most interested in the variety of customers in their database along with theri purchasing behaviours. Of course, one size does not fit all when it comes to marketing strategies. Therefore, our primary focus is to dissect customer diversity and purchasing behaviors to devise targeted marketing campaigns.

# Tools and Techniques
For this analysis, I utilize Python as my primary tool for analysis and for data visualization. Leveraging the power of Python, I employ various libraries including:
* NumPy for numerical computations
* Pandas for data manipulation and analysis
* Seaborn and Matplotlib for data visualization

Further, the following techniques are employed throughout the analysis:
* Data Cleaning and summarizing
* Data Wrangling
* Data Merging
* Deriving New Features
* Population Flows
* Creating Customer Profiles

By harnessing the capabilities of these tools and techniques, I aimed at extracting valuable insights from the data and presented them in a clear and concise form. 

# Datasets 
We have used open-source data sets from Instacart. Below is the link to the dataset I have used.
[Instacart Dataset](https://gist.github.com/jeremystan/c3b39d947d9b88b3ccff3147dbcf6c6b)

### Challenges
All the sales data we have is only for year 2017. Hence, we must keep in the relevance of this analysis before interpreting the results. I resolved the below listed problems with the dataset:
* Some of the products information was missing. I removed this missing data as it constituted less than 5% of the total data points.
* Removed first_name and last_name from the dataset for security reasons and they were not needed for the analysis.
* The missing values for days_since_prior order was retained as for the first order of a customer days since prior order will be NA.

Apart from the challenges with the dataset, creating customer profiles using the data was difficult. The most challenging part was to decide which features to keep and which features should be dropped while creating customer profiles as there were a number of possibilities for customer profiles. 

Note: I would be recreating the customer profiles using machine learning algorithms such as clustering to create more reliable customer profiles. Updates regarding which will be posted here.


# Key Questions
There are a number of questions that can be asked using this dataset. In this project, I answered the following key questions:

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


# Results
Following in an excerpt from the results of the analysis to give you an overview of the resutls. For complete results please read read the Report. [Link to the final Report](https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/commit/f10d4b9d9eb6ec4d7dd1d17135068f5238ecc2b8)

One of the questions were to find the busiest days and hours of the week. 
<div align="center">
<img width="537" alt="image" src="https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/assets/153047871/f21610e5-d4b0-4c1b-b244-fd367169ddff">
<img width="540" alt="image" src="https://github.com/b-N-I-R-A-V/Instacart_Basket_Analysis/assets/153047871/cbf6ec0e-a30e-4fe0-b663-8f23b7f43b5b">

</div>


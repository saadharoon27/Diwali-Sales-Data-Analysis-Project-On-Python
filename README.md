![banner](Assets/Banner.jpg)

# Diwali-Sales-Data-Analysis-Project-On-Python
***A company seeks an exploratory analysis of their Diwali sales data to boost revenue and customer experience. The analysis covers sales by region, product categories, and customer behaviors, aiming to identify trends and opportunities. The goal is to provide actionable recommendations for strategy refinement, enhanced engagement, and revenue growth.***

## Author
- [@saadharoon27](https://github.com/saadharoon27)

## Table of Contents
- [Business Problem](#business-problem)
- [About The Dataset](#about-the-dataset)
- [Method](#method)
- [Explore The Notebook](#explore-the-notebook)
- [Pre Analysis](#pre-analysis)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Suggestions](#suggestions)

## Business Problem
_A company has shared their Diwali sales data, seeking an exploratory data analysis to unveil valuable insights. With the ultimate objective of enhancing customer experience and boosting revenue, the analysis is aimed to deliver a summary of their sales data. By delving into their sales performance, identify trends, customer preferences, and potential opportunities for optimization._

_Our exploration will encompass a multifaceted examination of sales by region, product categories, and customer behaviours. We will pinpoint top-performing states and categories. The ultimate goal is to provide actionable recommendations that enable the company to refine strategies, enhance customer engagement, and create tailored initiatives that resonate with their audience. By leveraging the insights derived from the exploratory data analysis, the company can not only elevate customer satisfaction but also strategically increase their revenue, thereby charting a course toward sustainable growth._

## About The Dataset
![Diwali Sales Dataset](https://www.kaggle.com/datasets/saadharoon27/diwali-sales-dataset)

| **Column Name**        | **Description**                                     |
|--------------------|-------------------------------------------------|
| **User_ID**            | User identification number                      |
| **Cust_name**          | Customer name                                   |
| **Product_ID**         | Product identification number                  |
| **Gender**             | Gender of the customer    |
| **Age Group**          | Age group category of the customer             |
| **Age**                | Age of the customer                             |
| **Marital_Status**     | Marital status of the customer |
| **State**              | State of the customer's location               |
| **Zone**               | Geographic zone of the customer's location     |
| **Occupation**         | Occupation of the customer                      |
| **Product_Category**   | Category of the sold product                    |
| **Orders**             | Number of orders placed by the customer        |
| **Amount**             | Amount spent on purchases by the customer      |
| **Status**             | Empty Column         |
| **unnamed1**           | Empty Column   |

## Explore The Notebook
To explore the notebook click ![**here**](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/blob/f2a2ef06a6316d6f0c4fb6e86197e088b6bcb376/Project%20On%20Diwali%20Sales.ipynb)

## Method
_**Exploratory data analysis**_

## Pre Analysis
1. **Imported Libraries**: Libraries such as *numpy*, which facilitated intricate mathematical operations critical to the examination. Additionally, the imported *pandas*, enabling seamless data manipulation, comprehensive cleansing, and thorough exploration. *Matplotlib* and *seaborn* are also imported to further enriched the analysis, empowering the creation of compelling visual representations that will illuminate key insights within the dataset, thereby fostering a deeper understanding of the Diwali sales trends and dynamics. <br>

2. **Imported DataFrame**: The second step included the importing of the dataframe utilizing the `pd.read_csv()` function. To eliminate any potential encoding errors, the `'unicode_escape'` parameter was incorporated, ensuring the seamless importation of the dataset. <br>

3. **DataFrame Check**: To check whether the proper file has been imported with the exact data several codes, such as `df.shape` (returns the nrow, and ncolumns), and `df.head()` (Gives the overview of the first five rows), were passed. <br>

## Data Cleaning
1. **Passed `df.info()`**: By using `df.info()`, an assessment of the dataset was done, revealing key information on column data types, counts, and the existence of null values. Upon examination, it was found that some values of the 'Orders' column are missing, and all the values of 'Status' and 'Unnamed1' columns are missing.

2. **Dropping Columns**: Dropped 'Status' and 'Unnamed1' columns, as they do not contain any values using the `df.drop()` function.

3. **Dropping Null Values**: The 12 rows in the 'Orders' column were removed, which had null values. The choice of dropping those rows was made because the number of rows was insignificant compared to the total length of rows.

4. **Changing DType**: The 'Amount' column's datatype was modified from `float64` to `int32`, as decimal precision was unnecessary for the dataset's needs.

5. `df.describe()`: This function facilitated a deeper dive into the mathematical parameters of the data, enabling a more informed and insightful exploratory data analysis phase.

## Exploratory Data Analysis
- ***Gender***
  - For the purpose of dissecting the customer demography within the sales data, a **gender-based order count** was done. This examination revealed a predominant proportion of orders attributed to **'Female'** customers. A visual representation of this variation is illustrated in **Figure 1.1**.       <br>
    <br>
    - ***Figure 1.1:* Orders Created by Genders** <br>
     ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/fbdec8c3-b6ca-46a4-bdd5-bbdf5d7afc89)
  - After the initial analysis, I delved deeper into the data to understand the revenue contribution from each gender. The results revealed that **'Female'** customers have a notably higher contribution, almost double that of **'Male'** customers (Check Figure 1.2), emphasizing their significant role in driving the store's revenue. <br>
    <br>
    - ***Figure 1.2:* Revenue by Gender** <br>
    ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/f755304c-fa06-419f-a207-be278498e37c)
    <br>
    
    The above graphs reveals that most of the buyers are ***females*** and even the **purchasing power of females are higher than men**.
- ***Age:***
  - **Age group** plays an important part in data analysis as it is crucial and helps to identify target demographics, tailor marketing strategies, and understand consumer behaviour based on different life stages.
    
  - Analyzing orders generated by different age groups provides insights into purchasing patterns. This information can guide marketing efforts, and customer engagement strategies tailored to each age segment's needs and behaviors. **The Figure 2.1** shows the number of orders different age groups and genders generated.
    - ***Figure 2.1:* Order Count by Age Group**
      ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/a319ba6f-682d-4725-a5d6-1e362e1a3fb4)
   - As the number of orders does not truly represent the revenue generation, revenue contribution was also taken into account and analysed **(Figure2.2)**.
     - ***Figure 2.2:* Revenue by Age Group**
       ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/636f852a-ffa1-4cf7-bbf3-e6d95e991ee8)
    - The graphs clearly show that the majority of buyers fall within the **26-35 age range**, with a significant presence of female customers.
- _**Top States:**_
  - Identifying *top-performing* areas in terms of order generation helps allocate resources for a *stronger supply chain*, and focus on areas with high customer demand for optimized business outcomes. Taking this into consideration, and to analyse order geography, a bar chart representing the order count of *10 top-performing* states is plotted **(Figure 3.1)**.
    - ***Figure 3.1:* Orders Created by States**
    ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/5e14ba3e-5be0-482b-a422-586975cd68a0)
  - The best performers are **Uttar Pradesh,** followed by **Maharashtra, Karnataka, Delhi, Madhya Pradesh** and so on.
  - As previously highlighted, the count of orders alone might not always provide a comprehensive insight. Recognizing the significance of revenue as a key performance metric for a store, the analysis was extended to correlate the data with revenue contributions. This association is visually presented in **Figure 3.2**.
    - ***Figure 3.2:* Amount Spend by States**
      ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/573d81d6-af3a-42ad-8c5c-ebe05b76c1f6)
  - There is not much of a difference between the **Figure 3.1** and **3.2** graphs, expect the **8th** and **9th** place.

- ***Marital Status:***
  - _Does marital status effect the purchase behaviour of the customers? And if yes, then how does it affect the behaviour of the customers?_
    - ***Figure 4.1:* Orders Created by Marital Status**
      ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/386d68e7-9209-4352-b230-27ec3ead4097)
  - The observation reveals that individuals categorized as **'Married'**, **'0'** exhibit a greater count of orders, totaling 6518, in comparison to 'Single' customers labeled as '1', who recorded a lower order count of 4721. This discrepancy might arise from the augmented combined income of a family unit, which inherently translates into higher purchasing capability. Alternatively, this trend could stem from an increased demand for various products to meet the diverse needs of multiple family members.
  - Does the married person generate more revenue for the store also?
    - ***Figure 4.2:* Amount Spend by Marital Status**
      ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/0545eb59-15cf-4c9f-bdbd-eec90d22eb37)
  - This pattern is also evident in the value of goods they purchase **(Figure 4.2)**. Most of the buyers are married **(Female)**.
- ***Customer Occupation:***
  - A customer's occupation can significantly impact their purchasing power, as it directly correlates with the amount they spend. Customers with more lucrative occupational backgrounds tend to have a greater expenditure capacity compared to those in less lucrative fields. This trend is effectively depicted in the graph provided below **(Figure 5.1)**.
    - ***Figure 5.1:* Amount Spend by Occupation**
      ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/de1586f2-ae07-42d0-8075-12545ca18ec2)
  - From above graph we can see that most of the spenders are working in **IT, Healthcare** and **Aviation** sector.
- ***Product Category:***
  - It's important to ensure a consistent stock availability for product categories that exhibit rapid sales turnover, even if these categories might not be the highest revenue generators. The graph depicted in **Figure 6.1** illustrates the sales performance across various product categories, highlighting those that experience swift turnover.
    - ***Figure 6.1:* Orders By Different Categories**
      - ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/7a112ce2-89ac-47ac-aa5d-44f4646dd80e)
    - Now, the categories with the highest sales are **(Figure 6.2)**:
      - ***Figure 6.2:* Revenue By Product Categories**
      ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/5a37d4ba-abcb-4f14-88be-17110cdb5d3b)
    - ***Figure 6.3:* Products With the Highest Sales**
      - ![image](https://github.com/saadharoon27/Diwali-Sales-Data-Analysis-Project-On-Python/assets/147087623/01daedf0-792d-4f01-b60a-e9f0be61a765)
    - **Food, clothing** and **electronics** are the _top 3_ highest revenue generating categories, followed by **footwear**. While the _3_ best selling products are **Product ID: _P00265242, P00110942, P00237542_**.

## Suggestions
In the pursuit of enhancing customer experience and driving revenue growth, an extensive analysis of the Diwali sales data has yielded valuable insights

1. **Gender Dynamics and Sales**: The analysis highlights a notable gender-based trend, where _'Female'_ customers emerge as the dominant contributors to both order count and sales volume. This indicates an opportunity to tailor marketing strategies and product offerings to cater to the preferences and needs of female customers.

2. **Age Segmentation**: The age group between _26 and 35_ stands out as a pivotal demographic, boasting the highest order frequency and revenue generation. Conversely, as age increases, revenue generation tends to decrease. To maximize profitability, consider targeting marketing efforts and promotions towards the lucrative _26-35_ age bracket.

3. **Regional Insights**: Regions like _Uttar Pradesh, Maharashtra, and Karnataka_ exhibit strong order contributions and revenue generation. Conversely, _Gujarat and Haryana_ lag behind. Leveraging these regional insights can aid in refining supply chain and distribution strategies to cater to high-performing areas and tapping into untapped markets.

4. **Marital Status and Purchasing Power**: _Married female_ customers are revealed as possessing the highest purchasing power. This group could potentially be targeted with premium products and personalized offers, thereby maximizing revenue potential.

5. **Occupational Affiliations**: Customers employed in _IT, Healthcare, and Aviation sectors_ demonstrate a robust propensity for higher sales value. Tailored offerings and engagement strategies for these segments could yield significant revenue gains.

6. **Product Category Dynamics**: Identifying the best-performing categories such as _Food, Clothing, and Electronics_ can inform inventory management and stocking decisions. On the contrary, categories like _Beauty, Auto, and Stationary_ should be scrutinized for improvement opportunities.

7. **High-Performing Products**: A few products, with IDs _P00265242, P00110942, and P00237542_, stand out as the best-selling. Ensuring the availability and promotion of these products can further boost overall sales and revenue.

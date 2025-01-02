# Telecom Customer Churn SQL Project

## Breakdown
- [Project Overview](#project-overview)
- [Process](#process)
- [Recommendations](#recommendations)
## Project Overview
---
This project addresses customer churn using SQL to analyze telecom data. Customer churn, or customer attrition, is when customers or subscribers stop doing business with a company or cease using its products or services. Churn can occur for various reasons, including dissatisfaction with the product or service, competitive offerings, pricing issues, personal circumstances, or poor marketing and communication.

In this project, SQL was utilized to analyze multi-year customer data to identify churn patterns and the factors influencing customer attrition. Advanced SQL techniques were employed to extract insights, calculate Customer Lifetime Value (CLV), and conduct an in-depth analysis using data exploration, cleaning, window, and aggregate functions. The goal was to provide actionable recommendations for enhancing customer retention and minimizing churn using SQL only.

## Data Sources
The dataset used in this project is the **Telco-Customer-Churn.csv**, located in the project file. This dataset contains customer information for a telecom company, including details such as customer demographics, subscription plan, and churn status.

## Tools
- **SQL**
- **MySQL Database**

## Process
The data was provided in CSV format and loaded into a MySQL database as a table named `datasets.telco-churn`. SQL queries were then used to clean, explore, and analyze the data, providing insights into churn patterns, customer demographics, and service features.

## Data Cleaning
1. **Checking for Duplicates**: Identified any duplicate records based on `customerID` to ensure unique customer data. No duplicates were found in the dataset.
2. **Null Value Checks**: Checked for missing values in key columns such as `SeniorCitizen`, `tenure`, and `TechSupport`. No null values were found in these columns, which are critical for analysis.
3. **Data Type Validation**: Ensured that columns like `TotalCharges` and `MonthlyCharges` were correctly formatted as numeric types to allow for aggregation and analysis.

## Exploratory Data Analysis (EDA)
- **Gender Distribution**: Analyzed the distribution of customers by gender, finding an almost equal split between male (3,555) and female (3,488) customers.
- **Churn Distribution**: Found that 26.54% of customers had churned, while 73.46% had retained their subscriptions.
- **Churn by Gender**: 
  - Female churn rate: 26.92%
  - Male churn rate: 26.16%
- **Income Revenue by Gender**: Calculated the total charges generated by male and female customers, showing no significant gender-based differences in revenue.

## Data Analysis
### Churn Analysis:
1. **Senior Citizen Churn Rate**: Senior citizens have a significantly higher churn rate (41.68%) compared to non-senior customers (23.61%).
2. **Partner Churn Rate**: Customers without a partner have a higher churn rate (32.96%) compared to those with a partner (19.66%).
3. **Churn by Tenure**: 
   - The churn rate is highest for customers with less than 12 months of tenure (47.68%).
   - The churn rate decreases as tenure increases, reaching as low as 6.61% for customers with more than 60 months of tenure.
4. **Streaming TV Impact**: Customers with no internet service or streaming TV have a significantly higher churn rate. For example, customers without streaming TV had a churn rate of 33.52%.
5. **Churn Rate by Monthly Charges**: Customers paying between $50 and $100 per month had the highest churn rate (32.67%).

### Customer Lifetime Value (CLV):
- **CLV Analysis**: The CLV per customer was calculated based on tenure and monthly charges. Customers with longer tenures tend to generate higher total charges, leading to an increased CLV. The CLV per customer could not be calculated due to issues with non-numeric data in the `TotalCharges` column.

## Family Analysis
- **Churn by Family Status**:
  - **Family** (Partner and Dependents): These customers have a lower churn rate compared to others, suggesting greater stability.
  - **Partner (No Dependents)**: This group exhibits a moderate churn rate.
  - **Dependents (No Partner)**: Customers with dependents but no partner had a relatively higher churn rate.
  - **Single**: Single customers have the highest churn rate, indicating that customers without family connections may feel less loyal to the service.

## Results and Findings
1. **High Churn for Senior Citizens**: Senior citizens have a much higher churn rate than non-senior customers. Targeted marketing or service modifications could help retain this group.
2. **New Customers Are More Likely to Churn**: Customers with less than 12 months of tenure are more likely to churn. Improving the early customer experience might reduce churn in this group.
3. **Gender and Partner Status**: Gender doesn’t seem to play a major role in churn, but partner status does. Customers without a partner are more likely to churn.
4. **Streaming Services**: Customers with internet and streaming services show lower churn rates. Offering these services more widely could improve retention.
5. **Targeting Single Customers**: Single customers (without partners or dependents) exhibit the highest churn rate. This group could benefit from loyalty programs or offers designed to increase engagement.

## Recommendations
1. **Target Senior Citizens**: Tailor promotions or service offerings for senior citizens to reduce churn in this demographic.
2. **Improve New Customer Experience**: Focus on improving the onboarding process for new customers (with less than 12 months tenure) to prevent early churn.
3. **Offer Benefits for Families**: Customers with dependents or partners tend to stay longer, so offering special benefits for families might further reduce churn in this segment.
4. **Enhance Streaming Services**: Invest in enhancing or expanding streaming services, as customers who use these services show lower churn rates.
5. **Offer Incentives to Singles**: Create retention programs specifically for single customers to reduce their higher churn rates.

## Reference 
- Kaggle for the dataset

*P.S*: I wrote this code a while ago to show my SQL proficiency 😄, If you would like to recreate this project or have interesting questions you can reach out to me.


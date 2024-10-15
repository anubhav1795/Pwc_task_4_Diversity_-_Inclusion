# Pwc_task_4_Diversity_-_Inclusion
Pwc Switzerland Power BI virtual case experience - Diversity and Inclusion Analysis
Problem Statement

**The purpose of this analysis is to:**

Define proper KPIs in hiring, promotion, performance and turnover.

Create a visualisation for the HR manager that reflects all relevant Key Performance indicators(KPIs) and metrics in the dataset.

The following measures could help to define proper KPIs:

'#' of men

'#' of women

'#' of leavers

% employees promoted (FY21)

% of women promoted

% of hires men

% turnover

Average performance rating: men

Average performance rating: women

Data Sourcing
The Dataset used for this analysis was presented by Pwc Switzerland and available at:

Diversity Inclusion Dataset

Data Preparation
Data transformation was done in Power Query and the dataset was loaded into Microsoft Power BI Desktop for modeling.

The diversity and inclusion dataset is given by a table named:

HR Manager which has 32 columns and 500 rows of observation


Data Cleaning for the dataset was done in power query as follows:

Unnecessary columns were removed

Unnecessary rows were filtered

Each of the columns in the table were validated to have the correct data type
Data Visualization
Data visualization for the dataset was done in 3 folds using Microsoft Power BI Desktop:


![Screenshot 2024-10-15 181406](https://github.com/user-attachments/assets/978ecbd6-d0c7-4227-9f17-021027b4cf87)
![Screenshot 2024-10-15 181500](https://github.com/user-attachments/assets/2f5c22d4-37c3-491f-98ad-4cf4873fbb6a)
![Screenshot 2024-10-15 181543](https://github.com/user-attachments/assets/872c9ac1-4b6e-48c3-86c0-8637d7a62514)


**Data Analysis**
Measures used in visualization are:
'# Avg Female Rating = CALCULATE(AVERAGE('Pharma Group AG'[FY20 Performance Rating]),FILTER('Pharma Group AG','Pharma Group AG'[Gender] = "Female"))
'# Avg Men Rating = CALCULATE(AVERAGE('Pharma Group AG'[FY20 Performance Rating]),FILTER('Pharma Group AG','Pharma Group AG'[Gender] = "Male"))
'# Female = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="Female"))
'# Male = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="Male"))
'# Promoted FY20 = CALCULATE(COUNT('Pharma Group AG'[Employee ID]),'Pharma Group AG'[Promotion in FY20?]="Y")+CALCULATE(COUNT('Pharma Group AG'[Promotion in FY21?]),'Pharma Group AG'[Promotion in FY21?]="Yes")
'# Employee Turnover = DIVIDE('Pharma Group AG'[#Leaver],COUNT('Pharma Group AG'[Employee ID]),0)
'# Leaver = CALCULATE(COUNT('Pharma Group AG'[FY20 leaver?]), 'Pharma Group AG'[FY20 leaver?]="Yes")
 % of Female = DIVIDE( 'Pharma Group AG'[Number of Female],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])
 % of Male = DIVIDE( 'Pharma Group AG'[Number of Male],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])

**Insights**

As shown by Data Visualization, It can be deduced that:

💠 Total employees count was 500 out of which 295 are men and 205 are women 

💠Avg Rating women 2.42%

💠Avg Rating women 2.41%

💠The most common age group is 20-29 having 215 employees fall in this category.

💠 Men's Performance rating was slightly higher than Women's Performance Rating.

💠 Women are less promoted compared to men.

💠 The turnover rate of men was higher than women.

💠The HR department has more women count than men 

💠Almost all departments have greater men count than women except for HR and Operations Department Women's count was very less in Executive, Director, and Senior Manager job level




# Macdonald_data
This data is MacDonald data that includes response regarding taste, health, cost and efficiency. Further, it also includes responders age, visit frequency and ratings. 

**Methodology**

**Data cleaning and validation**
The data cleaning and validation steps are summarized in figure 1. The data types of each column were explored. Most of the columns were object datatype except Age columns which was an int64 data type. The unique values in each column were studied. The unique values looked okay for yummy, convenient, spicy, fattening, greasy, fast, cheap, tasty, expensive, healthy, and disgusting columns (2 unique values: yes and no). The unique value for Like columns were ratings from -5 to 5; however, -5 and 5 were labelled as 'I hate it!-5' and 'I love it!+5' respectively. The values 'I hate it!-5' and 'I love it!+5'  were changed to -5 and 5 respectively. The unique value for gender looked okay (Male and Female). The unique values for visitfrequency were 'Every three months' 'Once a week' 'Once a month' 'Once a year', 'More than once a week' and 'Never'. These unique values were converted to values as visit frequency per year as shown in figure description. There were 22 number of duplicated rows. Since there was no unique identifier for any of these columns and the possible values range was low it was difficult to decide if these rows were true duplicates or were coincidentally duplicates. Hence, I decided to check for subsequent duplicate rows and remove only those rows. There were no missing values. The summary statistics did not show any extreme values for Age column. The data type for columns yummy", "convenient", "spicy", "fattening", "greasy", "fast", "cheap", "tasty", "expensive", "healthy", "disgusting" and "Gender" were converted to category data type. The Like and visitfrequency columns were converted to integer data type. Further, additional columns age_group and visits per year were created based on the Age and visitfrequency columns. Both columns are category data types. 

![data_cleaning_validation_summary](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/2d25e81a-8a9b-4eac-ac1d-31f539dcc589)

Figure 1. The summary of data cleaning and validation steps. The data were checked for data types, unique values, duplicates and summary statistics. All columns except Age were object data type. The data types were converted to category data type for most of the columns except like and frequency. The duplicates values in subsequent rows were removed. The summary statistics did not show any extreme values for Age column. The unique values were okay for most of the columns. For columns Like and visitfrequency, the unique values were replaced. The like columns had values ranging from -5 to 5; however -5 and 5 were labelled as 'I hate it!-5' and 'I love it!+5' respectively. The values 'I hate it!-5' and 'I love it!+5'  were changed to -5 and 5 respectively.  The unique values for visitfrequency were 'Every three months' 'Once a week' 'Once a month' 'Once a year', 'More than once a week' and 'Never'. These values were converted to number of visits per year and replaced as follow: (Every three months: 4,  Once a week: 52, "Once a month": 12, "Once a year": 1, "More than once a week": 156, "Never": 0). For more than once a week, the visits were assumed to be 3 times a week on average. Additional columns age_group and visits_per_year were created using Age and visitfrequency columns. The ages were categorized as "16-20 y", "21-25 y", "26-30 y","31-35 y", "36-40 y", "41-45 y", "46-50 y", "51-55 y", "56-60 y", "61-65 y" and ">65 y" in age_group column. The visits_per_year column was a category datatype of visitfrequency column and the value 156 was replaced with >52. 


**Statistical Analysis**


**Results**


**Response regarding taste, health, cost, and efficiency of the restaurant**


The columns were categorized as features related to taste, cost and efficiency and health. The taste related features were “Yummy”, “Tasty”, “Spicy” and “Disgusting”. The cost and efficiency related features were “Cheap”, “Expensive”, “Fast” and “Convenient”. The health-related features were “Healthy”, “Fattening” and “Greasy”. The overall response analysis suggested that the responders are comparatively satisfied with features related to taste and cost and efficiency; however, they are not satisfied with features related to health. Higher percentages of respondents commented to positive taste related features as Yes (yummy: 55.23% and Tasty: 64.39%) and negative taste related features as No (Spicy: 90.63%, Disgusting: 75.69%) (Figure 2). Similarly higher percentages of respondents commented the restaurant to be cheaper, fast, and convenient (yes %: cheap (59.85%), expensive (35.81%), fast (90.01%), convenient (90.77%)). Higher percentages of respondent commented the food to be unhealthy, fattening, and greasy (yes %: healthy (19.9%), fattening (86.71%), greasy (52.62%)). 


![data_distribution_taste](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/2cb0c368-92de-42c0-986f-12f45c540cf9)

Figure 2. Percentage distribution of response regarding food taste. A) Yummy,  B) Tasty, C) Spicy, D) Disgusting. Overall the respondent comments regarding taste of food looks comparatively satisfactory. Higher percentages of respondent commented Yes for positive taste related features (A, B) whereas higher percentages of respondent commented No for negative taste related features (C, D). 


![data_distribution_efficiency](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/44437456-53d9-4780-8ab7-ac05de1ed065)

Figure 3. Percentage distribution of response regarding restaurant cost and effiency. A) Cheap, B) Expensive, C) Fast, D) Convenient. Overall, the rspondent commented the restaurant to be cheaper, fast and convenient. 


![data_distribution_health](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/69317825-5750-4515-aa22-d97b16ba6d6d)

Figure 4. Percentage distribution of response regarding health. Overal, the respondent seemed unsatisfied with features related to health. Higher percentages of respondent commented food to be unhealthy, fattening and greasy.



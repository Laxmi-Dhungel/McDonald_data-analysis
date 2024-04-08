# Macdonald_data
This data is MacDonald data that includes response regarding taste, health, cost and efficiency. Further, it also includes responders age, visit frequency and ratings. 

**Methodology**

**Data cleaning and validation**


The data cleaning and validation steps are summarized in figure 1. The data types of each column were explored. Most of the columns were object datatype except Age columns which was an int64 data type. The unique values in each column were studied. The unique values looked okay for yummy, convenient, spicy, fattening, greasy, fast, cheap, tasty, expensive, healthy, and disgusting columns (2 unique values: yes and no). The unique value for Like columns were ratings from -5 to 5; however, -5 and 5 were labelled as 'I hate it!-5' and 'I love it!+5' respectively. The values 'I hate it!-5' and 'I love it!+5'  were changed to -5 and 5 respectively. The unique value for gender looked okay (Male and Female). The unique values for visitfrequency were 'Every three months' 'Once a week' 'Once a month' 'Once a year', 'More than once a week' and 'Never'. These unique values were converted to values as visit frequency per year as shown in figure description. There were 22 number of duplicated rows. Since there was no unique identifier for any of these columns and the possible values range was low it was difficult to decide if these rows were true duplicates or were coincidentally duplicates. Hence, I decided to check for subsequent duplicate rows and remove only those rows. There were no missing values. The summary statistics did not show any extreme values for Age column. The data type for columns yummy", "convenient", "spicy", "fattening", "greasy", "fast", "cheap", "tasty", "expensive", "healthy", "disgusting" and "Gender" were converted to category data type. The Like and visitfrequency columns were converted to integer data type. Further, additional columns age_group and visits per year were created based on the Age and visitfrequency columns. Both columns are category data types. 

![data_cleaning_validation_summary](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/2d25e81a-8a9b-4eac-ac1d-31f539dcc589)

Figure 1. The summary of data cleaning and validation steps. The data were checked for data types, unique values, duplicates and summary statistics. All columns except Age were object data type. The data types were converted to category data type for most of the columns except like and frequency. The duplicates values in subsequent rows were removed. The summary statistics did not show any extreme values for Age column. The unique values were okay for most of the columns. For columns Like and visitfrequency, the unique values were replaced. The like columns had values ranging from -5 to 5; however -5 and 5 were labelled as 'I hate it!-5' and 'I love it!+5' respectively. The values 'I hate it!-5' and 'I love it!+5'  were changed to -5 and 5 respectively.  The unique values for visitfrequency were 'Every three months' 'Once a week' 'Once a month' 'Once a year', 'More than once a week' and 'Never'. These values were converted to number of visits per year and replaced as follow: (Every three months: 4,  Once a week: 52, "Once a month": 12, "Once a year": 1, "More than once a week": 156, "Never": 0). For more than once a week, the visits were assumed to be 3 times a week on average. Additional columns age_group and visits_per_year were created using Age and visitfrequency columns. The ages were categorized as "16-20 y", "21-25 y", "26-30 y","31-35 y", "36-40 y", "41-45 y", "46-50 y", "51-55 y", "56-60 y", "61-65 y" and ">65 y" in age_group column. The visits_per_year column was a category datatype of visitfrequency column and the value 156 was replaced with >52. 


**Statistical Analysis**
https://pingouin-stats.org/build/html/generated/pingouin.pairwise_tests.html

**Results**


**Response regarding taste, health, cost, and efficiency of the restaurant**


The columns were categorized as features related to taste, cost and efficiency and health. The taste related features were “Yummy”, “Tasty”, “Spicy” and “Disgusting”. The cost and efficiency related features were “Cheap”, “Expensive”, “Fast” and “Convenient”. The health-related features were “Healthy”, “Fattening” and “Greasy”. The overall response analysis suggested that the responders are comparatively satisfied with features related to taste and cost and efficiency; however, they are not satisfied with features related to health. Higher percentages of respondents commented to positive taste related features as Yes (yummy: 55.23% and Tasty: 64.39%) and negative taste related features as No (Spicy: 90.63%, Disgusting: 75.69%) (Figure 2). Similarly higher percentages of respondents commented the restaurant to be cheaper, fast, and convenient (yes %: cheap (59.85%), expensive (35.81%), fast (90.01%), convenient (90.77%)). Higher percentages of respondent commented the food to be unhealthy, fattening, and greasy (yes %: healthy (19.9%), fattening (86.71%), greasy (52.62%)). 


![data_distribution_taste](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/2cb0c368-92de-42c0-986f-12f45c540cf9)

Figure 2. Percentage distribution of response regarding food taste. A) Yummy,  B) Tasty, C) Spicy, D) Disgusting. Overall the respondent comments regarding taste of food looks comparatively satisfactory. Higher percentages of respondent commented Yes for positive taste related features (A, B) whereas higher percentages of respondent commented No for negative taste related features (C, D). 


![data_distribution_efficiency](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/44437456-53d9-4780-8ab7-ac05de1ed065)

Figure 3. Percentage distribution of response regarding restaurant cost and effiency. A) Cheap, B) Expensive, C) Fast, D) Convenient. Overall, the rspondent commented the restaurant to be cheaper, fast and convenient. 


![data_distribution_health](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/69317825-5750-4515-aa22-d97b16ba6d6d)

Figure 4. Percentage distribution of response regarding health. Overal, the respondent seemed unsatisfied with features related to health. Higher percentages of respondent commented food to be unhealthy, fattening and greasy.


**Who visited the restaurant most often?/ How often did they visit the restaurant?**

The median age for the respondent was significantly lower for the respondent who visited the restaurant more often. The median age of respondent who never visited the restaurant was 55 whereas the median age of the respondent who visited more than 52 times a year was 33 (Figure 5). The median age of respondent who visited few times or never (0, 1, 4 times as year) was significantly lower than the respondent who visited more frequently (12, 52 and > 52 times a year) (Mann-whitney test, sig (p<=0.05)). Most of the respondent visited restaurant 12 times a year (Figure 6). Similarly, most of the respondent in age group 16- 50 years and > 65 years visited the restaurant 12 times a year whereas most of the respondent in the age-group 51-65 years visited the restaurant 4 times a year (Figure 7). Highest number of visit frequency for both male and female was 12 times a year (Figure 7). 


![median_age_visits_per_year](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/12575c65-d8f4-455c-b96f-c1f7aeddf1d2)

Figure 5. Median age of respondent based on their visit frequency per year. The age of respondent who visited more often (12, 52 and >52 times a year) was significantly different than the age of respondent who visited less often (0, 1 and 4 times a year) (Mann-whitney test, sig (p <=0.05)). The lesser visit frequency and higher visit frequency are separated by red dashed line. Further, within lesser visit frequency the median age of respondent who visited restaurant 4 times a year was significantly lower than who never visited the restaurant. Similarly, within the higher visit frequency the median age of respondent who visited 52 times a year is significantly lower than the respondent who visited the restaurant 12 times a year. 


![visits_per_year](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/0446b066-77f7-4b75-b077-13cc3af43e5e)

Figure 6. The percentages of respondent based on their visit frequency per year. Most of the respondent visited the restaurant 12 times a year (30.17%) whereas the least percentages of the respondent visited the restaurant > 52 times a year (3.72%).


![relative_percentages_age_gender](https://github.com/Laxmi-Dhungel/Macdonald_data/assets/154451345/b43982c6-bc90-4bde-ba54-61dd4a91b3e0)

Figure 7. Relative percentages of number of visits based on A) age-group and B) gender. Most of the respondent in age-group 16-50 years (>30%) and > 65 years (28%) visited the restaurant 12 times a year. Most of the respondent in age-group 51-65 years (29%) visited the restaurant 4 times  ayear. Similary, for both gender the highest visit frequency was 12 times a year (>30%). The relative percentage of respondent was least (<5%) for visit frequency > 52 times a year for age group 16-20 and >31 years. For age-group 21-30 least percentages of respondent (<5%) never visited the restaurant. Similarly, for both gender the lowest visit frequency was >52 times a year (< 5%). 




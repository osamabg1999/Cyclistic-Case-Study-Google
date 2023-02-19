![alt text](https://github.com/osamabg1999/Cyclistic-Case-Study-Google/blob/main/cycle.jpg?raw=true)
# Case Study: Convert Casual Cyclistic Riders to Annual Members: Case Study
This case study was the capstone project for my Google Data Analytics Certification.

## Links
- [Presentation](https://docs.google.com/presentation/d/1z2YCNgDSn-9SV6pwoq-A5kl4HvwHY47kgS5KLy1f_84/edit#slide=id.p)

- [Case Study](https://d3c33hcgiwev3.cloudfront.net/aacF81H_TsWnBfNR_x7FIg_36299b28fa0c4a5aba836111daad12f1_DAC8-Case-Study-1.pdf?Expires=1676678400&Signature=Ivvf0r~BHgaaysgK~6zpoN~9ZMehC-lesen2f9G8zTCsTzDcqYX-qWFlG3nyRjcsrQ~TW6BOzseQXm5~EWDXoVUvy~4uHAiuc-cP5IuNlm2wLCfJkcW7S3ScSeHzsWHuGbX494e-xeJ67IC9EcV5HLAsUSnLbBuvZIg3zLo64dU_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

The script and presentation have also been uploaded in this repository.

## Scenario
You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

## About Cyclistic
In 2016, Cyclistic launched a successful bike-sharing offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unloacked from one station and returned to any other station in the system anytime.
Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

## The Stakeholders
- Lily Moreno: The director of marketing and my manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program.
- Cyclistic marketing analytics team: A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy.
- Cyclistic executive team: A notoriously detail-oriented team which will decide whether to approve the recommended marketing program.

## The Business Task
The goal of this case study is to provide clear insights for designing marketing strategies aimed at converting casual riders into annual members. Towards this goal, I asked the following questions:
*How do annual members and casual riders use Cyclistic bikes differently?
*Why would casual riders buy Cyclistic annual memberships?
*How can Cyclistic use digital media to influence casual riders to become members?

## Data Cleaning and Processing

### Tools
To process the data from dirty to clean, I used Python since it is faster and handles huge datasets well. 
### Cleaning the data
The first step in data cleaning was to identify which columns and rows had missing data after reading in and combining the 12 datasets into a single dataframe.
I indexed into the first and last missing data rows and discovered that they had null values on multiple columns. I also calculated the percentage of rows with missing values (22.8%). After reviewing the columns with missing data, I determined that imputation would be an incorrect approach due to the nature of the missing data. I decided to remove the rows with missing values because they account for such a small percentage of our data and appear to have missing values on multiple columns.
After removing missing data rows, I checked to see if any of the remaining observations had duplicates. There were no duplicate rows. I was confident that the data was ready for further processing and analysis after this step.

## Data Transformation
When I looked at the data summary after cleaning the data, I noticed that the started at and ended at columns were strings rather than datetimes. As a result, I converted the columns to datetime using the pandas to datetime() function.
Then, to leave exactly 12 months of data, I deleted the data for February 2023. To create the ride length column, I calculated the difference between the started at and ended at values. As a result, a time delta object was created, which I converted to seconds and then minutes.
I added two more columns: days of the week and month names. These particulars include the weekday and month of rental.
I obtained the summary to ensure that the data was ready for analysis, and I discovered that the ride length column contained negative integers. I filtered the rows with negative ride length data to further investigate them. Closer inspection revealed that the negative values were caused by the ended at day or time being shorter than the started at. Only 69 rows displayed this phenomenon, prompting their removal.
Finally, I received the data summary and concluded that the data was ready for analysis.

## Data Analysis
I analyzed the cleaned data in this step to determine how annual members and casual riders use Cyclistic bikes differently.
First, I determined the total number of bikes hired and how they were distributed among casual and member riders. Following that, I looked at how total bike hires were distributed per month and then per day. This revealed some intriguing trends, which I will discuss further in the share stage.
Next, I looked at how bike hires between the two types of riders compared in a given month and day of the week. The goal at this point was to determine whether casual riders preferred certain days or months over member riders.
Next, I wanted to compare the average ride length of casual riders and member riders. When compared to member riders, casual riders tend to ride for longer periods of time. I was intrigued and decided to investigate how the average ride length compares on a daily and monthly basis for both rider categories.
Finally, I compared the types of bikes hired by the two rider categories.

## Sharing Insights
In order to convey the findings of my analysis, I used the seaborn and matplotlib tools in this stage. This repository contains the generated visuals and insights. In my presentation, I used the same graphics.

## Recommendations
The results showed a clear difference between bike usage by casual riders and annual members in summer months and weekends. To encourage more casual riders to become annual members, the following recommendations were made:

- Launch a summer promotion that targets casual bike riders. Offer a discount on bike rentals for casual riders during the summer months. This could incentivize more casual riders to rent bikes
- Create a weekend-specific promotion to encourage more weekend rentals. Offer a free rental day for every two days rented on a weekend.
- Create a loyalty program that rewards frequent casual riders with discounts or other incentives. This could encourage more repeat business from this group and help build a loyal customer base.


# ( UBer Data Analysis )

## Table of contents

- [Overview](#Overview-of-Dataset)
  - [Dataset](#Content-of-Dataset)
  - [Root Cause Analysis Process](#root-cause-analysis-process)
  - [Key Insights](#Observationa-and-Insights)
  - [Built with](#built-with)


## Overview of Dataset
Uber is a multinational transportation network company that operates a platform connecting riders with drivers through a mobile app. It was founded in 2009 and has since become one of the most well-known examples of a ride-hailing service. Uber allows users to request a ride from their current location to a desired destination using their smartphone. The app matches the user with an available driver in the area, and the driver arrives to pick up the passenger.

Uber offers various types of services, including UberX (standard car), UberXL (larger vehicles), UberBlack (luxury vehicles), and UberPOOL (shared rides with other passengers traveling in the same direction). The fares for rides are calculated based on factors such as distance traveled, time spent on the trip, and demand at the time of the request.

Uber has gained popularity for its convenience, ease of use, and competitive pricing compared to traditional taxi services. It has expanded its operations to numerous cities around the world and has also introduced other services like food delivery (Uber Eats) and package delivery (Uber Connect).


## Content of Dataset

- This dataset contains a csv file of containing Customer Drives Data of `START_DATE`, `END_DATE`, `CATEGORY`, `START`,`STOP`, `MILES`and `PURPOSE` respectively for 1155  records.

- All column variables throughout the dataset includes :

- `START_DATE`: Timestamp that marks the start of the trip.
- `END_DATE`: Timestamp that marks the end of the trip.
- `CATEGORY`: Uber customer category.
- `START`: Location that marks the start of the trip.
- `STOP`: Location that marks the start of the trip.
- `MILES`: Travel distance.
- `PURPOSE`: Customer's purpose of ordering Uber.


## Root Cause Analysis Process
To ascertain a root cause analysis, we attempted to answer the followimg questions with the newly created tables

1. How many Uber trips occurred during the timestamp in the dataset?
2. What is the median for daily, weekly and monthly total trips?
3. How is the customer segment proportion? 
4. What are the favorite pick-up spots for each segment?
5. How is the hourly trend for Uber trips?
6. How is the daily trend for Uber trips?
7. How is the monthly trend for Uber trips?
8. Is there any specific characteristic of each segment based on the travel duration?
 


## Observationa and Insights

- The data start to record 1154 trips from 1 Jan 2016 to 31 Dec 2016 (1-year timestamp)

- 4 orders each day (based on median measurement) or we can say that there is 1 order for every 6-hour
- 51 order per week (based on median measurement) or we can say more than 7 orders per day
- 110 orders each month (based on median measurement)
						
- Throughout 2016, 1077 Uber Drives for Business purposes, compared to only 77 Uber Drives were for Personal use.
- The top 3 purpose for our customers to order Uber is Meeting, Meal/Entertain, and Errand/Supplies, all of which lies in the category of Business.
- If from the very first start, the company does prioritize targeting business people, this result wouldn't be so much of a concern. However, if the company also indeed target Personal use customer, this result is concerning and thus needs to be investigated more.				
						
- The orders start to increase at 6 a.m.
- There are a relatively high amount of orders starting from 1 pm to 6 pm.
- Apparently, there was no Uber order made at the time interval 4 a.m. - 5 a.m. in 2016.						

- Surprisingly, orders are less likely to occur on Wednesdays than on weekend days.
- Orders are skyrocketing on Friday.
- Low orders on the weekend can be associated with the customer segment proportion which implies ~93% of customers are ordering Uber for business purposes. 
					
- The orders are increasing and considered in the relatively high amount in Q1.
- The orders are declining at the beginning of Q2 but increase at the end of the quarter.
- In Q3, it increased at the beginning of the quarter, however, it declined steeply at the end of the quarter.
- And the order experienced a good increasing trend in the last quarter (Q4).

- We can see that our trip duration data also consists of many outliers.
- On the median, customers who have Errand/Supplies purpose tend to have relatively low travel duration.
- Customers with Meal/Entertain purposes have relatively low travel duration compared to other purposes in the Business category.
- On a median, customers who have Meetings, Customer Visits, Temporary Sites, and Between Offices purposes have similar travel duration.
- Customers who have Customer Visit purposes have relatively higher variability than the other purposes.



### Built with

- Python (JupyterNotebook)
- Data Cleaning and Processing : Numpy , Pandas
- Visualization : matplotlib, Seaborn

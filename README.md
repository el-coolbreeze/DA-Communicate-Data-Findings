# Ford GoBike System Data
## by Umar Abubakar


## Dataset Overview

> The original dataset contained rides taken during the month of February 2019. Effort was made to gather additional data for the remaining months of 2019. Due to 
Ford GoBike website being offline and other repositories not having data for the months of May and beyond, we were only able to gather additional data for the months
of January, March and April of 2019 bringing the number of months worth of data to four (4).
Additional data was gathered from (https://s3.amazonaws.com/fordgobike-data/index.html).

> The dataset contains 870904 rides taken during the months of January to April of 2019 with 16 attributes namely:
- duration_sec
- start_time
- end_time
- start_station_id
- start_station_name
- start_station_latitude
- start_station_longitude
- end_station_id
- end_station_name
- end_station_latitude
- end_station_longitude
- bike_id
- user_type
- member_birth_year
- member_gender 
- bike_share_for_all_trip

## Summary of Findings

> Before exploring the dataset, an assumption was made that the distance between the start_station and end_station location would affect the duration of each ride. 
An assumption was also made that age of the members, user_type, member_gender also determines the number rides taken. Findings include:

- Univariate Exploration: In this exploration, we used histograms to visualize the distribution of individual numeric variables, pie charts and barcharts to visulaize the 
  proportion of individual categoricalvariable and we were able to discern the following information:
  
  - The analysis on the duration_sec variable showed that majority of the rides were short and under 2,000 seconds.
  - The distribution of the age variable showed that majority of the customers are between the age of 20 and 80 years. It also showed that a few of the users
    are over 100 years old. Wrong date of birth information maybe?
  - The distance of most rides is between 0.3km and 10km with the peak distance travelled for most rides at 1km.
  - The analysis of the user_type variable shows that most of Ford GoBike users are Subscribers, 86.7% of them while the remaining 13.3% are Customers.
  - The analysis of the member_gender variable show that majority of Ford GoBike users are male (74.1%) and 24.0% are female while 2.0% are other (did not specify their gender).
  - Of the four months of Ford GoBike systems data analysed, March recorded the highest number of rides closely followed by April and then January and February.
  - Analysing the day of week variable showed that majority of the rides were taken during the week days while the weekends saw less rides.
  - Analysing the time_of_day variable showed that a lot of users take rides during the Morning, followed by Evening and Afternoon. Night has the lowest number of rides recorded.
  
- Bivariate Exploration: in this exploration, we analyzed the relationships between pairs of variables and made follwing observations:
  
  - Using the median value which is less susceptible to outliers to visualize the trends of duration and distance between January to April, we see that 
    there was a decline in the duration and distance of rides taken from January to February and that while duration increased from February to April, 
	distance increased from February to March followed by a sharp decrease between March and April.
  - Duration vs Distance: After removing the outliers from duration and distance, we observerd that there is a positive correlation between the distance 
    and duration variables.
  - Duration vs Age: After removing the outliers from duration and age, we observed that majority of Ford GoBike members are between the age of 20 and 50 
    years with younger members clocking the highest durations.
  - Member gender vs Duration: We observed that female members took longer rides than other (unpecified gender) and males. This is the case despite male 
    members having a higher proportion than females.
  - User Type vs Duration: The relationship we observed from the user_type and duration_sec variables is that cutomers took longer rides than subsribers.
  - Time of Day vs Member Gender: The relationship showed that males, females and other prefer taking rides in the morning followed by afternoon and evening. 
    The time_of_day with the least number of rides observed for all gender's is night.
	
- Multivariate Exploration: in this exploration, we analyzed the relationships between three or more variables and observed the following:

 - duration_sec, age and member_gender: The scatter plots showed that there is high number of females that are between the age of 20 and 40 
   that take long duration rides while male members between the age of 20 and 60 years also take long duration rides. It also showed that 
   there is a larger proportion of males that take short duration rides than females. Members with unpecified gender (other) that are between 
   the age of 20 and 40 take rides that have a duration of about 1000 seconds.
 - duration_sec, distance and member_gender: The scatter plots showed that there is a similar trend (a positive correlation between duration_sec 
   and distance) for all categories of gender for Ford GoBike members and that the proportion of males taking short distance rides is larger than 
   that of females and Other (unspecified gender).
 - Between Ford GoBike customers and subscribers, customers tend to take the longest rides at all times of the day, on all days of the week and 
   also in all the months (January - February) of data analysed.
 - Between Males, Females, and Other (Unspecified gender), females take the longest rides followed by Other and Males at all times of day, 
   on all days of the week and in all four months of data analysed except in January where Other (Unspecified gender) was slightly higher than 
   females. Males have rides with the shortest durations.
 - distance and categorical variables: On average, in terms of distance, between Males, Females and Other (unspecified gender), Other take the 
   longest rides at all times of day except in the morning where females take longer rides, on all days of the week except on Thursday where females 
   take longer rides, and in all the months (January - February) of data analysed. At all times of day, on all days of the week and in all the months, 
   men took rides with the shortest distance.

  
## Key Insights for Presentation

> Key Insights for presentation include:
 - There was a decline in the duration and distance of rides taken from January to February and that while duration increased from February to April, 
   distance only increased from February to March followed by a sharp decrease between March and April.
 - Females and other take the rides with the longest duration despite the proportion of male members being larger.
 - Between Ford GoBike customers and subscribers, customers tend to take the longest rides at all times of the day, on all days of the week and also 
  in all the months (January - February) of data analysed despite the proportion of subscribers being larger.
 - The positive correlation between duration and distance for all gender types.
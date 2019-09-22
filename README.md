*The bikeshare folder includes the jupyter notebook and slides. Also a pdf describing some graphs used for exploring the data.*

# Ford-Go-Bike-Systems
The dataset in this repository was retrieved from https://lyft.com/bikes/bay-wheels/system-data for all the files in the year of 2018.
Lyft's bikeshare system is currently based in San Francisco County, Alameda County, and Santa Clara County.

## The Pricing
Lyft's bike share system offers three different types of pricing.
A **single ride** costs $2 for one ride up to 30 minutes. However, after 30 minutes it costs an extra 3$ per additional 15 minutes.
There is also a **monthly membership** available. For just $15 a month a member can ride unlimited 45 minute trips, however after 45 minutes there is an extra $3 per additional 15 minutes.
If a monthly wasn't enough there is a **annual membership**, where riders can pay $149 for the whole year. Like the monthly membership there is a limit of 45 minutes per trip and an additional $3 per extra 15 minutes after the initial 45 minutes.

## So how can we increase revenue?
We can look to target advertisements into riders who ride for long durations. 
By looking at the duration of each trip and comparing into other features we can look for patterns, and see which type of members tend to rider for longer period of time.

## Features in the original data
Trip Duration (seconds)
Start Time and Date
End Time and Date
Start Station ID
Start Station Name
Start Station Latitude
Start Station Longitude
End Station ID
End Station Name
End Station Latitude
End Station Longitude
Bike ID
User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)
Member Year of Birth
Member Gender

## Addtional features after cleaning the data
The longitude and latitudes were used in order to find the county's associated with each location.
The members year of birth was converted into age by subtracting the year of birth from 2018.
Trip duration was converted from seconds into minutes.
Both the age and duration of trips were categorized and binned accordingly.
A month column was also created for each trip.


## Intial Steps
Before diving right in and exploring the impact of the many features on the duration of the trips. Each feature was explored by itself. Firstly the distribution of the duration of the trips was explored. It was found out that most trips were shorter than 20 minutes. Which led to the question why are majority of the trips so short? Then the age was explored, it was found out that most of the riders were in their 20's and 30's, however one interesting thing to note was that there were much more 33 year olds than any other ages. Perhaps, the year 1985 is set to default when signing up? User gender was then explored, interestingly there were more than 2x more male users than female users. After checking for the genders, user status was found, and wow, most of our users are subscribers. There were about 5x as many subscribers then non subscribers. Maybe the membership is priced too low? The pattern of bike use for each month was explored as well. And as expected, most of the users rode during the hotter months, or during the  months of may, june,july, august,september, and october. And lastly, it was found out that most of the users started their trips in San Francisco County.

## Duration vs Features
So now we can start answering some questions. What patterns can we see when exploring the duration of trips against other features?
When looking at the duration of trips with the age of the users it was found out most of the users rode for under 200 minutes. However there were many people around 40 years and younger who also rode above 200 minutes. There weren't that many older people or those under 70 that rode for over 200 minutes, except for 1 outlier. Interestingly, when looking at the age vs subscriber it was found out that most users that were not subscribers were 33 years old. Which means that maybe the users that were not subscribers tended to use 1985 as their fake birth year. When looking at the duration of trip vs the month, users rode less on the month of november and december. Interestly duration of trip during october was also low, however when looking at just the frequency of the month, many people rode during october. When looking at the duration vs the county. The duration of the trips for each county was similar, with the averages being between 13.5 -14.5 minutes.

## Combining Features
The duration of the trips on the month/gender was explored. However, it was noted that both genders followed a similar pattern in the duration of trips, Where duration seemed to higher in the hotter months and lower in the colder months. However, interestingly for females the duration of trips in february was rather high. The average duration of trips on the subscription status/age was also found. Age was categorized into two, old and young, with young being anyone under 55 years old. Both the age groups were similar in average duration of trips. The duration of trips and the month/subscription status was also explored. Overall, many non-subscribers rode for longer durations throughout the months. Subscribers rode mostly shorter durations under 200 minutes. Subscribers also rode for longer periods during the warmer months (May, June, July, August).

## So what now?
We should target advertisements to females, because females ride for longer than males.
We should also start advertisements during the summer, or specifically July, as the number of users is high during july and the average trip is also high. We should also target non-subscribers, or maybe increase the membership fees. Members tend to ride for short periods as they seem to take advantage of their unlimited rides. 

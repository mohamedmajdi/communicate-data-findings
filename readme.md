# Bay Wheels Ride Data Exploration and Visualization
## by Mohamed Majdi Abdelsattar


## Dataset

> Bay Wheels (previously known as Ford GoBike) is a regional public bike sharing system in the San Francisco Bay Area, California. Bay Wheels is the first regional and large-scale bicycle sharing system deployed in California and on the West Coast of the United States since the launch in 2017. The dataset used for this exploratory analysis consists of monthly individual trip data from January 2019 to December 2019 in CSV format covering the greater San Francisco Bay area, also available here: https://s3.amazonaws.com/baywheels-data/index.html

### Data wrangling process:
* fix columns that are not in the correct dtype, i.e. start_time, end_time should be datetime type, user_type should be categorical data type, etc
* add new columns for trip duration in minute, trip start date in yyyy-mm-dd format, trip start hour of the day, day of week and month
* cast 'start_dayofweek' to ordered category dtype for easy plotting
* cast 'start_month' to ordered category dtype for easy plotting

## Summary of Findings

> The number of trips peaked around 8-9am and 17-18pm during a day, there were more trips on work days (Mon-Fri) compared to weekends. Summar time was the most popular season of a year, likely due to the weather. The riding trips tend to be shorter on Monday through Friday compared to weekends. It indicates a pretty stable and efficient usage of the bike sharing system on normal work days, while more casual flexible use on weekends.

> There are a lot more subscriber usage than customers overall. The riding habit/pattern varies a lot between subscribers and customers. Subscribers use the bike sharing system for work commnute thus most trips were on work days (Mon-Fri) and especially during rush hours (when going to work in the morning and getting off work in the afternoon), whereas customers tend to ride for fun in the afternoon or early evenings over weekends. Subscriber usage peaks out on typical rush hours when people go to work in the morning and getting off work in the afternoon, which strengthened their usage purpose and goal of riding. Similar pattern was not observed among customers who tend to ride most in the afternoon or early evening for a different purpose than the subscribers.


## Key Insights for Presentation

> Different usage pattern/habit between the two type of riders are seen from the exploration. Subscribers use the system heavily on work days i.e. Monday through Friday whereas customers ride a lot on weekends, especially in the afternoon. Many trips concentrated around 8-9am and 17-18pm on work days for subscribers, yet customers tend to use more in the late afternoon around 17pm Monday to Friday. The efficient/short period of usage for subscribers corresponds to their high concentration on rush hours Monday through Friday, indicating the use is primarily for work commute. The more relaxing and flexible pattern of customer use shows that they're taking advantage of the bike sharing system quite differently from the subscribers, heavily over weekends and in the afternoon, for city tour or leisure purpose probably.

## Resources
> https://stackoverflow.com/questions/37400974/unicode-error-unicodeescape-codec-cant-decode-bytes-in-position-2-3-trunca
> https://stackoverflow.com/questions/2512386/how-to-merge-200-csv-files-in-python
> https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html
> https://strftime.org/
> https://seaborn.pydata.org/tutorial/aesthetics.html
> https://matplotlib.org/3.1.1/gallery/pie_and_polar_charts/pie_and_donut_labels.html
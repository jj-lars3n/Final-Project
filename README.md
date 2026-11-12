# Final Project
https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand?resource=download
https://colab.research.google.com/drive/1O0SkCPo0hXLPE6rYI4JL7sqBKtsv_-Yu?usp=sharing
# HOTEL BOOKING ANALYSIS PYTHON FINAL PROJECT

About 42% of city hotel bookings in my dataset were canceled compared with about 28% of resort hotel bookings. I checked when guests planned to arrive, how far in advance they booked and how often they canceled. August had the most scheduled arrivings and January had the fewest. City hotel guests also tended to book a tad further ahead. That higher cancellation rate matters because that can mean that even when a hotel has a lot of reservations planned some people might not show up.

## Data Cleaning

I found missing values in the children, country, agent, and company columns.

To clean the data I replaced missing children values with 0. Replaced missing country values with "Unknown". Filled missing agent and company values with 0. Changed the children column to integers. Checked for duplicate rows and found 31,994. I decided to keep them because some could be separate bookings with the same information.

After cleaning I checked again and there were no missing values left.

## Data Manipulation

I used a few different methods to organize the data and make it easier to analyze. Filtering: I filtered the dataset to only show canceled bookings using is_canceled == 1. Grouping: I used groupby() to calculate the average cancellation rate for each hotel type. Sorting: I used value_counts() to see which countries had the most bookings, sorted from highest to lowest.

I also created a new column called total_nights by adding weekend nights and weekday nights together.

## Visualizations

#### 1. Cancellation Rates by Hotel Type

My first graph is a bar chart comparing the cancellation rates between city hotels and resort hotels. City Hotels had a cancellation rate of about 41.73% while Resort Hotels had a cancellation rate of about 27.76%.This shows that city hotels had a higher percentage of cancellations.

<img width="576" height="457" alt="image" src="https://github.com/user-attachments/assets/bf79bfdb-e5d2-4234-8cc4-c7946918f265" />


#### 2. Bookings by Month

My second graph is a bar chart showing how many bookings were made for each arrival month. I wanted to see which months were the busiest and whether there were differences in booking activity throughout the year. The graph shows that some months have a lot more bookings than others.

<img width="1023" height="549" alt="image" src="https://github.com/user-attachments/assets/06f6eaf9-8d49-4f1d-ad7a-484b1924db3d" />


#### 3. Booking Lead Time by Hotel

My third graph is a box plot comparing how far in advance people booked city hotels and resort hotels. I chose a box plot because it makes it easier to compare the spread of booking lead times and see outliers. Both hotel types had some bookings made hundreds of days in advance.

<img width="850" height="549" alt="image" src="https://github.com/user-attachments/assets/1166b989-417d-43b3-b8ba-ac4dabd474e2" />


## Statistical Analysis

I calculated the mean, median, and standard deviation for booking lead times.

Mean: 104 days

Median: 69 days

Max: 737 days

Standard Deviation: 106.86 days

The average booking was made about 104 days before arrival, but the median was only 69 days. This suggests that some very early bookings increased the average. I also calculated the correlation between lead time and cancellations. Correlation: 0.293 This is a positive correlation, meaning bookings made further in advance tended to have a higher chance of being canceled. However, the relationship isn't especially strong.

## What I Learned

This project helped me practice importing data, cleaning missing values, filtering, grouping, and creating graphs with python libraries. I learned that booking lead time has some relationship with cancellations and that people sometimes make hotel reservations way farther in advance that I previously thought. Overall this project helped me get more comfortable using pandas, seaborn and especially matplotlib to analyze data .

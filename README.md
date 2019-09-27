# How Busy Is The Gym Right Now?
Who wants to go to an overcrowded gym? Wouldn't it be great to see when the best time to go is? Or even just to know what to expect when you're planning to head in?

This is something I've always been curious about, and now it's finally something I can create!

## Objective
In the grand scheme of things, I want to create a chart that displays the expected number of people in the gym for each hour. This chart would be updated daily.

Using weather forecasting, holidays, events, and class schedules, the occupancy should be predictable.

## Data Collection
Understanding the gym's sign-in procedure (scanning a fob key upon entry), I gathered the sign-in data from GymMaster. GymMaster is the gym's organizational platform that stores/collects data about membership information and activity. This data includes timestamps of members signing in and their member ID.

For weather information I used the [DarkSky API](https://darksky.net/dev) using the location of Victoria, British Columbia.

## Assumption
The data acquired only shows when members sign in, and not when they sign out. So we have no exact reading of how many members are in the gym at a given moment. 

Therefore, I had to assume that members would spend roughly 1.5 hours in the gym upon signing in.

Why did I choose an hour and a half? I've been a member for over a year and have learned a few things:
- Most members spend between 1-2 hours in the gym (some outliers spend more than that but only a handful of people)
- Classes are one hour in length, by the time members sign in, warmup, do the class, and cool down/talk with others after it's been about 1.5 hours

## Sections
There are four different sections that make up this project:

Weather Data Collection - Collecting the hourly weather data and exporting to a csv

Occupancy Data Collection - Using the sign-in data to gather occupants per hour and exporting to a csv

Occupancy Data Exploration - Analyzing the occupancy data and providing commentary

Weather vs Occupancy - Using the two above csv's, combine them and perform predictive analysis

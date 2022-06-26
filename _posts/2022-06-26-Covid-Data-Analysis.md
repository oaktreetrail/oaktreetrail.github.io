COVID_Data_Analysis
================
2022-06-026

In this project, I created seven functions (get_Data, countries_Names, countries_Names_pop, get_Date, get_Country, get_confirmed_data and get_all_data) to interact with the coronavirus API. The data were pulled from three endpoints (Summary, By Country and All Status By Country). First, I plotted spatial data to show the coronavirus cases in the world map. This map indicated that the United States of America had the largest total confirmed cases, followed by India and Brazil. This conclusion was confirmed by the coronavirus case summary by country. Europe had the largest total confirmed cases, while America had the largest total deaths.Then, I created a histogram to show that most of the countries had less than 20% of their population contracted the coronavirus. These proportions were up to roughly 60% in some countries. The scatter plot showed us that log2(TotalConfrimed) and log2(TotalDeath) had a roughly linear relationship among countries. Since the US had the largest numbers of cases, I further looked into the data in the US. California had the highest case numbers in the period of Jan 1, 2022 to May 31, 2022, followed by Florida and Texas. In California, Los Angeles had the most days with daily cases greater than 5,000. And the cases surged in Jan 2022 in Los Angeles, CA.

The most difficult part of the programming is to create functions to read in a one-week data set and loop through a period of time, and then combine them together. Since the case numbers were cumulative, I need to revert them back to individual values. These new variables were created one by one. In the future, I would use apply() function to create these variables at once.

[COVID_Data_Analysis](https://oaktreetrail.github.io/ST558_Project_1/)

[COVID_Data_Analysis_Github](https://github.com/oaktreetrail/ST558_Project_1)


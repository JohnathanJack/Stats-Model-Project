# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The goal of this project is to use CityBikes API to gather and create a list of locations(latitude and longitude) of bike stations all around Toronto, ON. This list of coordinates will be used with Yelp and FourSquare API to determine the number of restaurants, the restaurants ratings and total photos of the restaurant within 1km of each bike station. This data will be combined into a data frame where it will be analyzed to determine if there are any correlation between the variables and the number of bikes. A regression model will be created from the data frame to determine if there wasa any significance between each variable. 

## Process
1. Created a function to take in a city and determine the network id
2. The network id will be used in another function to create a dataframe containing the number of bikes at each location and their coordinates
3. Created a function for Yelp and FourSquare API to get information in a 1km radius of restaurants, their ratings and total number of photos
4. Create two different data frames for each API and compare their information
5. Combined the two data frames from Yelp and FourSquare and start analyzing the data
6. Created scatterplots,histoplot and heatmaps for the number of bikes vs each variable
7. Create a linear regression model for only yelp and foursquare data and the combined data frame
8. Analyze for any correlation

## Results
There was no correlation between the number of bikes and the number of restaurants. This may be skewed heavily as there were 26900 from Yelp and 16248 from FourSquare that had a showing of 50 restaurants(the limit from each API). There was an outlier that can be seen with almost 50 bikes at a very low restaurant count, but with further inspection it turned out to be at a beach. This gives insight on the other points of interests that may have an impact on the number of bikes. I performed the same test with subway stations but found that it had no correlation with the number of bikes as well using a heatmap. Those findings can be seen in the notebooks I created ending with transit. The merging did not have anything in common as both APIs had named each station differently or used an alternate entrance/exit address of the subway stations. 

## Challenges 
The challenge was working with two different APIs that had more than 50+ restaurants within 1km of the bike stations but unable to retrieve it. This caused an artifical wall at the 50 mark that may have severely lowered the correlation between the number of bikes and restaurants. Upon removing all restaurants that were 50, it was seen there was no correlation at all. I am unsure if I had complete data if this result would have changed. Upon merging the API's data frame together, only 655 were in common with eachother but there was a total of 56415 rows if an outer join as performed. This made it difficult to choose how I would work with the dataset and determining results. 

## Future Goals
I would love to try and explore other points of interests such as: educational institutions, tourist spots and shopping areas for any correlation with the number of bikes. 

# nosql-challenge

PART 1

First, I imported the establishments.json file from my terminal and identified uk_food as the database and establishments as the collection. These were both assigned variable names.

PART 2

The information from Penang Flavours was entered as a dictionary and inserted into the collection. 

The Business Type ID was located for the Restaurant/Cafe/Canteen type of business and I inserted it into the Penang Flavours dictionary.  

I used a query to find how many documents have the Local Authority Name as Dover.

Once located, all these documents were deleted and deletion was confirmed. 

Longitude and latitude were both changed from strings to decimals in order for future analysis to occur. 

PART 3

In order to establish which establishments have a hygiene score of 20, I queried the establishments that matched the hygiene score of 20 and converted the results to a DataFrame.

Next, I used $regex to find the establishments that had a Local Authority Name of London with a rating value of other 4 (using $gte). These results were also converted to a DataFrame.

To find the top 5 establishments with a rating value of 5 sorted by lowest hygiene score and nearest to Pengang Flavours, I used a variety of methods. First, I found the latitude and longitude of Pengang Flavours and calculated the range that the queried restaurants needed to be within. I queried the restaurants by matching the Rating Value equal to 5 and ensuring the latitude and longitude ranges were correct and sorted by hygiene. I converted these results to a DataFrame.

Finally, I used a pipeline to find the establishments in each Local Authority area with a hygeine score equal to zero. I converted these results to a DataFrame. 
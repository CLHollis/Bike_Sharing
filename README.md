<image src="images/b.jpg" width="900" height="500">[^1]
# Invest Now! DesMoines Bike Sharing Opportunity

## Overview of the statistical analysis

### Scenario
Your friend and you go to NYC and use the Citi Bikes to get around on your trip. You wonder if you could start a ride-share company in your hometown of Des Moines, IA. You and your friend have a possible investor but need to convince them it is a good idea using data.

### Process
1. Change the tripduration column data type to DateTime data type using Python/Pandas & Jupyter Notebook. [Here's the code](NYC_CitiBike_Challenge.ipynb)
  
      <image src="images/a.JPG" width="170" height="300">
      
      ```
      import pandas as pd
      import datetime
      # 1. Create a DataFrame for the 201908-citibike-tripdata data. 
      tripdata = pd.read_csv("201908-citibike-tripdata.csv") 
      tripdata.head(5)
      # 2. Check the datatypes of your columns. 
      tripdata.dtypes
      # 3. Convert the 'tripduration' column to datetime datatype.
      tripdata['tripduration'] = pd.to_datetime(tripdata['tripduration'], unit='s')
      tripdata.dtypes
      # 4. Check the datatypes of your columns. 
      tripdata.head(5)
      # 5. Export the Dataframe as a new CSV file without the index.
      tripdata.to_csv('revised_201908-citibike-tripdata.csv',index=False)
      # 5B.Check that the newly revised file has the updated tripduration column data
      revised_tripdata = pd.read_csv("revised_201908-citibike-tripdata.csv") 
      revised_tripdata.head(5)
      ```
        
2. Use Tableau to make some analysis
        
      <image src="images/c.JPG" width="400" height="200">
3. Create a story to share with investors: ["Invest Now! DesMoines Bike Sharing Opportunity"](https://public.tableau.com/views/BikeSharingChallenge_16461908237810/InvestNowDesMoinesBikeSharingOpportunity?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)

### Programs Used
- Jupyter Notebook 6.4.6
- Pandas
- Tableau Public v.2021.4
- [August 2019 NYC CitiBike Ride Sharing data](https://s3.amazonaws.com/tripdata/201908-citibike-tripdata.csv.zip)

## Results & Summary
These charts can be helpful to find target market, but in order to get investors, I would add a lot more about profit margins. Maybe pull in another dataset on the cost of runnning a bikeshare business and merge that with an estimate of DesMoines usage based on a ratio from the NYC volume and number of tourists attractions. 




<image src="images/1.JPG" width="800" height="800">
<image src="images/2.JPG" width="800" height="800">
<image src="images/3.JPG" width="800" height="800">
<image src="images/4.JPG" width="800" height="700">

[^1]: [bikes photo](https://www.thedataschool.co.uk/andy-kriebel/ds10-dashboard-week-day-4). Accessed March 1, 2022.


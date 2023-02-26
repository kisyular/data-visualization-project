# FordBike Exploration Project

## By: Rellika Kisyula

## Dataset

The Ford GoBike dataset contains anonymized trip data for the bike-sharing system from June 2017 to April 2019. **However, I decided to only use the data in the year 2018 (January 2018 to December 2018).** The data includes information on individual bike rides such as trip duration, start and end time, start and end station, bike ID, and user type. Additionally, demographic data such as age, gender, and membership type is provided for some users.

I manually downloaded the datasets from the [System Data | Bay Wheels | Lyft](https://www.lyft.com/bikes/bay-wheels/system-data) page. The datasets were in the form of a zip file. I extracted the zip files and saved the csv files in the `data` folder as this notebook. The zip files are in `data/zip_files` folder.

I then unzipped the files using `zipfile` and saved them in the `data/data_files` folder. I then read the csv files into a pandas dataframe and concatenated them into one dataframe. I then saved the dataframe as a csv file in the `data` folder as `bike_data.csv`.

### Wrangling Efforts

-   I added a column for the year, month, day, hour, and day of the week to the dataframe by extracting the information from the `start_time` column.
-   I calculated the distance travelled in kilometres using the `haversine` function and added it to the dataframe as `distance`.
-   I converted the `start_time` and `end_time` columns to datetime objects.
-   I also added a column for the age of the user by subtracting the birth year from the year the data was collected (2018).

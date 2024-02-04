Hello!

PROJECT TITLE:
Analysis on UK Food Hygiene Rating Data (London):
Food Hygiene Rating of Business in Boroughs of London in United Kingdom

Description:
The data provides the food hygiene rating or inspection result given to a business and reflects the standards of food hygiene found on the date of inspection or visit by the local authority. 
Businesses include restaurants, pubs, cafés, takeaways, hotels and other places consumers eat, as well as in supermarkets and other food shop.

Prerequisites:
. Knowledge on using Microsoft Excel
. Basic Knowledge on python 
. Knowledge on how to use Power BI  <https://www.udemy.com/course/data-analytics-essentials-with-power-bi/learn/lecture/17515464#overview>

Hardware: (The following specs were used to create the analytic report) 
. Windows 10 Pro [256gb boot disk]
. Intel(R) Core(TM) i7-6600U CPU, 16gb Memory

Software (The following apps were used to create the analytic report[visuals]):
.MS Excel 2021
.Microsoft Power BI [Version: 2.108.997.0 64-bit (August 2022)]

Installation:
. Power BI Desktop can be installed from Microsoft store directly into one's system
. Microsoft Excel can be used online or offline;
    - Online: through Office online from any available browser preferably Microsoft Edge <https://www.office.com/?auth=1> 
    - Offline: through Microsoft Excel app that can be downloaded from  <https://getintopc.com/softwares/office-tools/microsoft-office-2021-pro-plus-august-2022-free-download-6655620/>

Contributing:
Dataset: https://www.kaggle.com/datasets/datota/uk-food-hygiene-rating-data-london
UK postcode: https://raw.githubusercontent.com/gibbs/uk-postcodes/master/postcodes.csv

Data Setup: assuming the [https://www.kaggle.com/datasets/datota/uk-food-hygiene-rating-data-london] file is been downloaded
Below are the shell commands used in each step, as run from the top level directory
       kaggle competitions download -c <UK Food Hygiene Rating Data (London)> -food_hygiene_rating_data.csv

Data Preocessing:
 The Food Hygiene Rating DataSet mainly contains 12 columns;
Index(['FHRSID', 'LocalAuthorityBusinessID', 'BusinessName', 'BusinessType',
       'PostCode', 'RatingValue', 'RatingKey', 'RatingDate',
       'LocalAuthorityCode', 'LocalAuthorityName', 'Longitude', 'Latitude'],
      dtype='object')
but after loading/importing it into jupyter notebook, an 'Unnamed_0' column appears which stands like a serial number column.
so by <pd.read_csv("food_hygiene_rating_data.csv", index_col = 0)> removes the 'Unnamed_0' column, thereby retaining its initial number of columns

Data Visualization: There are 2 procedure to display the visuals
1)  By loading the dataset using MS excel 
      . and checking the data type of each column
      . changing the datatype of Rating Date, Local Authority code, Latitude & Longitude to 'text'
      . and then saving it to be loaded on Power bi Desktop
2)  By loading the saved dataset from Ms Excel on Power BI Desktop
     . after opening the app, move ahead to Get Data
     . and since our dataset is in csv format, we choose 'Text/csv
     . then transform data to do some additional changes
     . and the data is finally loaded on Power BI for proper visualization to begin

Insights: After a series of visulas on the dataset, some predictions were made
 . There is a linear correlation between food_hygiene_rating_data and Post code
 . Rating value "5" has noticeably more business name​
 . Restaurant/Cafe/Canteen' and 'Retailers -other' have noticeably more Business Name for Rating Key 'fhrs_4_en-GB'​

Conclusion:
In final conclusion, governments through Local authority needs to inspect thoroughly 
businesses with rating value of '2' and close/Lockdown businesses with rating value 
starting from 1 and below.​




 

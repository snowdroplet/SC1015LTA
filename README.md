# SC1015LTA
Code that creates a machine learning model for for analysing the the tap in volumes on the MRT network dependent on time, day, and station type. Data acquired is from LTA Datamall, for Jan 2025.

Please note:
If using the code for your own purposes, please download the dataset, and rename the file to what path it is on.
The columns of the dataset are as follows:

YEAR_MONTH: The month and year this was taken in. (For this dataset, all of the rows will be 2025-01, indicating Jan 2025.)
DAY_TYPE: On what type of day was this recorded. Broken into two types: WEEKDAY, AND WEEKEND/HOLIDAY
TIME_PER_HOUR: What hour was this recorded in. For example, a value of 12 indicates that the data was recorded from 1200hrs to 1259hrs (or 12:00-12:59pm). Values are 0, and then 5-23.
PT_TYPE: What of station it is (For this dataset, it's all TRAIN)
PT_CODE: The station code. First two letters indicates the line/service it is, and the next 2 numbers are the station on line. For example, BP10 means the 10th station on the Bukit Panjang LRT (in this case, Fajar)
TOTAL_TAP_IN_VOLUME: The number of tap-ins into the station within this hour.
TOTAL_TAP_OUT_VOLUME: The number of tap-outs into the station within this hour.

Data acquired from: https://datamall.lta.gov.sg/content/datamall/en.html (Third party API such as Postman required to collect data.)
Libaries used:
NumPy: https://numpy.org/
Pandas: https://pandas.pydata.org/
Scikit-learn: https://scikit-learn.org/
Seaborn: https://seaborn.pydata.org/
Matplotlib: https://matplotlib.org/

Project goal: To analyse the LTA dataset for passenger volumes in train stations, and find out when are the busiest times on the network.

How this was achieved:

Data cleaning: Removing unneccessary data such as PT_TYPE, TOTAL_TAP_OUT_VOLUME and YEAR_MONTH

Data preprocessing: Converting PT_CODE to station types, and then using OneHotEncoding to convert for modelling.

Machine learning: Using multiple predictors values, such as DAY_TYPE, station types, and TIME_PER_HOUR to get a better model, and using the Random Forest Regressor with edited parameters to get a better result.

Modelling: Creating a set of values for TIME_PER_HOUR, station type, and DAY_TYPE to acquire a set of predicted values for TOTAL_TAP_IN_VOLUME, and plotting that against TIME_PER_HOUR to create a time series graph.

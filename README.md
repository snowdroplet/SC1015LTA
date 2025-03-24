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

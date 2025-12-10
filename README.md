KOVAI.CO TECHNICAL REPORT
AMEEN AHMED H
BIT
1.	Dataset description
	This dataset contains daily public transport passenger journey data spanning from July 2019 to September 2024 (1,918 days of records). It tracks passenger volumes across six different service types.
Attributes: The dataset consists of daily passenger counts categorized by service type:
•	Date: Observation date.
•	Service Types: Local Route, Light Rail, Peak Service, Rapid Route, School, Other.
DATA PREPROCESSING
1.	Convert to Date feature to date type and sort using the date in increasing order.
2.	Replace Nan and 0 with forward fill and backward fill methods
3.	Remove outliers from the dataset.
 
Box plot to visualise outliers
<img width="801" height="425" alt="image" src="https://github.com/user-attachments/assets/6d0d141b-f240-4ef7-9c86-101a7652f4c5" />



Results of Preprocessing
The preprocessing pipeline resulted in a clean, temporally sorted dataset with no missing values.
•	Original Data Shape: (1,918 rows, 7 columns)
•	Rows Removed (Outliers): 11 rows
•	Final Data Shape: (1,907 rows, 8 columns)
2.	INSIGHTS FROM THE DATA
2.1.	Service Type Hierarchy 
Dataset has data from July 2019 to September 2024 and has critical patterns about public transport usage, demand dynamics, and business trends.
 <img width="716" height="355" alt="image" src="https://github.com/user-attachments/assets/53875a1c-fe66-4584-a6a0-513bc0d6cb7b" />

Rapid Route dominates with 37.3% of all journeys, followed by Local Routes (29.3%) and Light Rail (21.3%)
Rapid route leads public transport usage
2.2.	Annual Passengers Trend
From the data 
 <img width="573" height="284" alt="image" src="https://github.com/user-attachments/assets/60394b7c-8e16-4dd7-8c75-dff06959bd18" />

Annual passengers peaked in 2023 at 13.8M then declined 22.1% in 2024
Passenger growth peaks in 2023 then decline in 2024
2.3.	Weekend vs Weekdays
 <img width="672" height="333" alt="image" src="https://github.com/user-attachments/assets/9d8dcdab-4468-4865-a64e-4468af7c408e" />

Weekday commute traffic is 141% higher than weekends, peaking on Wednesday (42,238 avg)
Weekdays doubles weekends levels
2.4.	Seasonable Monthly Pattern
 <img width="803" height="398" alt="image" src="https://github.com/user-attachments/assets/fcd6062c-ab21-4889-a7ad-6672816c4039" />

Seasonality spikes
2.5.	Service Volatility across Transport services
 <img width="627" height="311" alt="image" src="https://github.com/user-attachments/assets/803991c7-8543-406d-84b2-982659600c5c" />

2.6.	Correlation matrix of service types
 <img width="940" height="804" alt="image" src="https://github.com/user-attachments/assets/603fdd59-cf5c-4a31-bd9b-fbadf232027a" />





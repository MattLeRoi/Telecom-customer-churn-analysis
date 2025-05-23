# Telecom Customer Churn Analysis

**Author**: [Matt LeRoi](mailto:mcleroi@gmail.com) 

Overview
Business and Data Understanding
  Explain your stakeholder audience and dataset choice here
Modeling
Evaluation
Conclusion

# Overview

In the telecom business, customers are generally on monthly or yearly contracts. The cost of acqusition of customers is high, so having sticky customers (customers that stick around once acquired and don't churn) is important. Therefore, predicting churn before it happens can reap huge financial benefits.

# Business Understanding

The goal of this project is to create a model to predict churn in customers for SyriaTel, a telecom company, before it happens so that a retention strategy can be implemented before they churn. SyriaTel has informed me that analysis of previous experiments shows that the estimated lost profit due to churn is ~$80/customer and the cost of outreach is ~$20/customer. The 

0   state                   3333 non-null   object 
 1   account length          3333 non-null   int64  
 2   area code               3333 non-null   int64  
 3   phone number            3333 non-null   object 
 4   international plan      3333 non-null   object 
 5   voice mail plan         3333 non-null   object 
 6   number vmail messages   3333 non-null   int64  
 7   total day minutes       3333 non-null   float64
 8   total day calls         3333 non-null   int64  
 9   total day charge        3333 non-null   float64
 10  total eve minutes       3333 non-null   float64
 11  total eve calls         3333 non-null   int64  
 12  total eve charge        3333 non-null   float64
 13  total night minutes     3333 non-null   float64
 14  total night calls       3333 non-null   int64  
 15  total night charge      3333 non-null   float64
 16  total intl minutes      3333 non-null   float64
 17  total intl calls        3333 non-null   int64  
 18  total intl charge       3333 non-null   float64
 19  customer service calls  3333 non-null   int64  
 20  churn                   3333 non-null   bool   
 


# Data Understanding

This project uses two data sources: [accident data](./data/Aviation_Data.csv) and [aircraft registration data](https://www.faa.gov/licenses_certificates/aircraft_certification/aircraft_registry/releasable_aircraft_download) from the FAA. The accident data, "data.csv", includes a unique entry for each accident or incident recorded, along with the number of injuries, fatalites, etc., information about the aircraft involved, and the circumstances around the event. The registration data contains a unique entry for each aircraft registered in the US and will be used to count the number of each make and model in operation. 

## Data Preparation

The large files are trimmed of unecessary information and formatted in a consistent manner to be merged later.

# Exploratory Data Analysis

The accident and registration data are merged, and rates of fatalities, injuries, occurrences of issues, etc. are calculated and displayed.

# Conclusion

The rates of aircraft issues varied greatly from aircraft to aircraft. Within the top 10 most common single and dual engine aircraft, the rates varied from 5 occurrances per 1000 registered aircraft to 25.  

![Tables.png](./Images/Tables.png)

There were no significantly noted differences in accident rates between single and dual engine aircraft. The number of people affected was different, however, due to the generally larger seating capacity of dual engine planes. 

![Stacked.png](./Images/Stacked.png)

![Bar_chart.png](./Images/Bar_chart.png)

## Limitations

The available data only provide the number of incidents, severity of injuries, and number of aircraft registered. Many other factors pertaining to the incidents could provide more detail about which incidents were related to the aircraft and which were pilot error, weather related, or otherwise independent of the aircraft. Also, the registration data seems a reasonable factor for normalizing incident counts, but number of hours or miles flown would be a more accurate normalization factor. 

## Recommendations

The following aircraft are recommended for further study:

Single engine aircraft:
- CIRRUS DESIGN SR22T
- PIPER PA-28-180
- PIPER PA-28-181

Dual engine aircraft:
- BD-100-1A10
- LEARJET INC 45
- BEECH 95-B55 (T42A)
- PIPER PA-23-250

## Next Steps

The recommended aircraft should be further analyzed for other factors, including:
- Acquisition cost
- Maintenance cost
- Fuel cost
- Staffing requirements
- Lifetime of aircraft / performance over time
- Availability of pilots and crew
- Seating capacity

## For More Information

See the full analysis in the [Jupyter Notebook](./Aircraft_safety.ipynb), review this [presentation](./Slides.pdf), or peruse this [dashboard](https://public.tableau.com/app/profile/matthew.leroi/viz/Aircraft_safety/Dashboard?publish=yes).

For additional info, contact Matt LeRoi at [mcleroi@gmail.com](mailto:mcleroi@gmail.com)

```
├── data
├── images
├── README.md
├── Slides.pdf
└── Aircraft_safety.ipynb
``` 

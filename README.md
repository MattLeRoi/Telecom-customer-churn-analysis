# Telecom Customer Churn Analysis

**Author**: [Matt LeRoi](mailto:mcleroi@gmail.com) 

# Overview

In the telecom business, customers are generally on monthly or yearly contracts. The cost of acqusition of customers is high, so having sticky customers (customers that stick around once acquired and don't churn) is important. Therefore, predicting churn before it happens can reap huge financial benefits.

# Business Understanding

The goal of this project is to create a model to predict churn in customers for SyriaTel, a telecom company. If customer churn can be identified before it happens, a retention strategy can be implemented before they churn. According to SyriaTel, the estimated lost profit due to churn is ~$80/customer and the cost of outreach is ~$20/customer. The cost of simply reaching out to all customers would be a net loss of $28,000, so accurate prediction of customers likely to churn will be extremely valueable here. If one customer is correctly identified out of every four customers flagged for potential churn, this project will be net neutral. The model will seek a much higher bar than that, however, and will optimize for maximum profit.

# Modeling

Two models were created for this project: 

# Evaluation




# Conclusion

The rates of aircraft issues varied greatly from aircraft to aircraft. Within the top 10 most common single and dual engine aircraft, the rates varied from 5 occurrances per 1000 registered aircraft to 25.  

![Tables.png](./Images/Tables.png)

There were no significantly noted differences in accident rates between single and dual engine aircraft. The number of people affected was different, however, due to the generally larger seating capacity of dual engine planes. 

![Stacked.png](./Images/Stacked.png)

![Bar_chart.png](./Images/Bar_chart.png)

## Limitations

The available data only provide the number of incidents, severity of injuries, and number of aircraft registered. Many other factors pertaining to the incidents could provide more detail about which incidents were related to the aircraft and which were pilot error, weather related, or otherwise independent of the aircraft. Also, the registration data seems a reasonable factor for normalizing incident counts, but number of hours or miles flown would be a more accurate normalization factor. 

## Recommendations

More data to refine the model to identify customers likely to churn more accurately.
Refinement of the outreach strategy - experiments can be run to determine the effectiveness vs cost of sending emails, making phone calls, offering discounts, etc. Analysis can also be perfomed to determine which outreach strategies are the most effective for different customer profiles (more models!).


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

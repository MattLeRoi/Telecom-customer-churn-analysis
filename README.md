# Telecom Customer Churn Analysis

**Author**: [Matt LeRoi](mailto:mcleroi@gmail.com) 

# Overview

In the telecom business, customers are generally on monthly or yearly contracts. The cost of acquisition of customers is high, so having sticky customers (customers that stick around once acquired and don't churn) is important. Therefore, predicting churn before it happens can reap huge financial benefits.

# Business Understanding

The goal of this project is to create a model to predict churn in customers for SyriaTel, a telecom company. If customer churn can be identified before it happens, a retention strategy can be implemented before they churn. According to SyriaTel, the estimated lost profit due to churn is ~$80/customer and the cost of outreach is ~$20/customer. The cost of simply reaching out to all customers would be a net loss of $28,000, so accurate prediction of customers likely to churn will be extremely valuable here. If one customer is correctly identified out of every four customers flagged for potential churn, this project will be net neutral. The model will seek a much higher bar than that, however, and will optimize for maximum profit.

# Modeling

Two models were created for this project: a logistic regression model and a decision tree classifier. These two were chosen because they can both handle making binary classification outcome predictions. Without knowing the type of relationship between the independent variables and the outcome (i.e. linear or more complex) beforehand, both models were created and compared. A baseline logistic regression model was created, then the data was scaled and oversampled (to combat the unbalanced data, since only 15% of customers churned). The baseline decision tree classifier was then created with various criteria and refined with hypertuning. During the tuning phase, a subset of the data was used for training and another set for validation. Once the parameters were set, the final evaluation was done using a final test set that wasn’t used during any of the training or tuning.

# Evaluation

The goal of this project is financial, to increase profits for SyriaTel. The recall and precision scores are relevant, as we are trying to identify as many of the churning customers as possible (recall rate) while limiting the number of customers we reach out to unnecessarily (precision rate). To combine these two scores, I have taken the estimate provided by SyraiTel to directly calculate the actual financial impact to the company. Each correctly identified churning customer (True Positive, TP) is worth $80 and every person SyriaTel reaches out to costs $20 (True Positie plus False Positive, TP+FP). The final evaluation criterion is then: $80TP + $20*(TP+FP), which is the total profit (or loss) of the experiment.


# Conclusion

The logistic regression model achieved a profit of $1660 after scaling and oversampling, correctly identifying 46 out of 101 churning customers, with 55 falsely identified churning customers. 

The final hypertuned decision tree classifier model outperformed the logistic regression model, achieving a profit of $4260 after hypertuning, correctly identifying 74 out of 101 churning customers, with 9 falsely identified churning customers. 

![Bar_chart.png](./Images/Bar_chart.png)

## Limitations

The available data covers a small number of customers and only includes basic usage and account data. It appears that there is enough to be useful, but more detailed data could be extremely helpful to refine the model further. Also, the financial evaluation is based on rough estimates, so further experimentation can refine the evaluation criteria.

## Recommendations

The model provided should yield positive results. However, broader data, covering more of SyriaTel’s customers and containing more varied and detailed information, should help refine the model. Also, 



> 264.45 day minutes, <= 6.5 voice mails, >184.65 eve min, > 114.5 night minutes = [2,80]
> 264.45 day minutes, > 6.5 voice mails = [38,5]
Don’t know why less voice mails means more churn. Also, at each stage, more minutes increases churn.

<= 264.45 day minutes, > 3.5 customer service calls, <=160.2 day minutes = [10,72]
More customer service calls is prob bad.

<= 264.45 day minutes, <= 3.5 customer service calls, with intl plan, <= 2.5 calls [0,39]
People with international plan that don’t use it will churn. Maybe offer to cancel the international part of their plan when you notice they’re not using it? 


<= 264.45 day minutes, <= 3.5 customer service calls, with intl plan, > 2.5 intl calls,>13.1 min [0,32]
Lower general usage, but higher than average international calls and higher international minutes causes churn. Maybe per minute cost is too high?

<= 264.45 day minutes, <= 3.5 customer service calls, with intl plan, > 2.5 intl calls,<=13.1 min [142,7]
Higher number of short calls - seems like people are happy. 


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

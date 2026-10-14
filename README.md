# Will the Customer Accept the Coupon?

Data analysis via pythod code and plot visualization for the data is from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. 

**Notebook:** prompt.ipynb

## Data
12,684 survey responses analyzed which describes number of different scenario (destination, time, weather, passenger),
the driver (age, income, habits), and the coupon offered (type, expiration).
`Y = 1` means the driver would accept the coupon.

**Cleaning:** dropped the `car` column (99% missing); filled the small number( less than 2%) of missing values for column non numberic columns - BAR, CoffeeHouse, CarryAway, ResturantLessThan20, Resturant20TO5o with the most frequently occured value determined using mode function.

## Summary of Findings

**Overall:** 56.8% of coupons were accepted. Carry-out and cheap-restaurant coupons were
accepted most often; bar and expensive-restaurant coupons least often.
Coupons acceptance percentage share- CoffeeHouese - 31.5%, Resturant(<20) - 22%, Carry out & Take away - 18.9%, Bar - 15.9% and Restaurant(20-50) - 11.8%

**Bar coupons (56.8% accepted):**
- Drivers who visit bars more than 3 times a month accepted 76.88% of bar coupons vs 37.07% for others.
- 70% of the bar goers more than once a month are over 25
- Frequent bar-goers without kid passengers accepted 70% vs 30% for others.
- **Takeaway:** bar coupons work best for existing regular bar-goers traveling without children.

**Coffee House coupons (49.9% accepted):**
- Acceptance peaked at 10AM and was lowest at 6PM.
- 1-day coupons outperformed 2-hour coupons for all the times of the day.

**Distance factor:**
- Coupon acceptance was same for the travel time 5-15 mins and 15-25mins but dropped for 25+ mins.


## Recommendations
-**Target coupons by past behavior:** Send bar and coffee coupons to drivers who already visit those venues regularly.
-**Time the offers:** Send Coffee House coupons early in the day, since drivers appear to prefer coffee before noon.
-**Prefer nearby venues:** Drivers accept more coupons for restaurants within a 25-minute drive, so limit coupons for venues farther away from the driver. 

## Next Steps
-Develop a machine learning model that analyzes all of the factors in detail to understand what influences drivers' decisions to accept coupons.
-Predictive analysis requires historical data to achieve higher accuracy, so I would like to work on building a historical dataset.
-Once the historical dataset is built and the model is developed, I would like to compare the model's predictions against actual survey data as it becomes available.


## References
AI tool is used to correct the grammer of the write up and to check the syntax of the python functions.
Anacode Jupter notebook AI tool is used to align the comments

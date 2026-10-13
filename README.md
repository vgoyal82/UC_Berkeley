# Will the Customer Accept the Coupon?

Exploratory analysis of the UCI "In-Vehicle Coupon Recommendation" survey data to identify
what distinguishes drivers who accept a coupon from those who reject it.

**Notebook:** 

## Data
12,684 survey responses describing a driving scenario (destination, time, weather, passenger),
the driver (age, income, habits), and the coupon offered (type, expiration).
`Y = 1` means the driver would accept the coupon.

**Cleaning:** dropped the `car` column (99% missing); filled the small number of missing
visit-frequency values (<2%) with the most common value.

## Summary of Findings

**Overall:** 56.8% of coupons were accepted. Carry-out and cheap-restaurant coupons were
accepted most often; bar and expensive-restaurant coupons least often.

**Bar coupons (41% accepted):**
- Drivers who visit bars more than 3 times a month accepted 77% of bar coupons vs 37% for others.
- Frequent bar-goers without kid passengers accepted 71% vs 30% for others.
- **Takeaway:** bar coupons work best for existing regular bar-goers traveling without children.

**Coffee House coupons (49.9% accepted):**
- Coffee house visit frequency was the strongest factor: ___% acceptance for regular visitors vs ___% for those who never go.
- Acceptance peaked at ___ and was lowest at ___.
- 1-day coupons outperformed 2-hour coupons (___% vs ___%).
- Acceptance dropped for venues 25+ minutes away (___%).

## Recommendations
- **Target coupons by past behavior:** send bar and coffee coupons to drivers who already visit those venues.
- **Time the offers:** send Coffee House coupons during ___; avoid ___.
- **Prefer nearby venues** on the driver's route, and use ___ expiration for coffee offers.

## Next Steps
- Build a predictive model (logistic regression or decision tree) to score each driver's likelihood of accepting.
- Extend the analysis to the remaining coupon types.
- Validate with real redemption data, since survey responses reflect stated intent.

# Executive Summary: Amman Digital Market
**A clear look at where we're winning and where we have room to grow.**

## Overview
We've taken a deep dive into our recent transaction data to see what's really driving sales across the Amman Digital Market. By looking at completed orders and weeding out any unusual data blips, we uncovered some clear takeaways about what our customers are buying and which cities hold the most untapped potential. 

## Top 3 Findings

### Finding 1: Electronics and Clothing are our high-value heavy hitters.
When people shop for Electronics or Clothing, they're spending significantly more. The average order for Electronics sits around 52 JOD, and Clothing follows closely behind at 48 JOD. On the flip side, categories like Food & Beverage typically sit at about 27 JOD per order.
* **The Math Behind It**: We ran an ANOVA test, which confirmed these categories don't just look different by chance—these spending habits are statistically significant.
* **Relevant Chart**: `category_aov.png`

### Finding 2: Amman is earning twice as much as Irbid, but not for the reason you might think.
Unsurprisingly, Amman is our biggest market, pulling in over 15,700 JOD compared to Irbid's 7,250 JOD. But here's the twist: a customer in Irbid spends almost exactly the same amount per order as a customer in Amman. Amman is only winning because they have more customers, not better customers.
* **The Math Behind It**: A T-test showed zero statistical difference ($p = 0.936$) in how much individuals in these two cities spend per checkout.
* **Relevant Chart**: `city_revenue.png`

### Finding 3: Our steady revenue growth leans heavily on our earliest customers.
Month-over-month revenue looks great. But if we break it down by when customers first signed up (their "cohort"), the people who joined us back in November and December of 2024 are still delivering the highest lifetime value. They keep coming back, which is fantastic, but we aren't seeing that same momentum with people who joined more recently.
* **Relevant Chart**: `kpi_trends.png` and `clv_cohorts.png`

## Recommendations

1. **Push ads for high-value items:** Since Electronics and Clothing reliably yield the best payout per cart, we should funnel more of our marketing budget into promoting these categories.
2. **Go big on customer acquisition in Irbid:** Since we know shoppers in Irbid are willing to spend just as much as those in Amman, we just need more of them. Let's invest heavily in brand awareness campaigns focused specifically on Irbid to boost volume.
3. **Win back our newer sign-ups:** Our earliest users stuck around, but newer ones need a nudge. We should launch an email sequence or a special promo campaign targeted at customers who registered in the last few months to get them back into the purchasing habit.

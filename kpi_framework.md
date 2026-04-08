# KPI Framework — Amman Digital Market

This is how we're tracking the health and growth of the Amman Digital Market. We've defined 5 core KPIs that tell us whether our efforts are actually paying off and where we need to course-correct.

---

## KPI 1: Monthly Revenue Growth
- **Name**: Monthly Revenue Growth (Time-based)
- **What it is**: The total revenue we bring in from completed orders each month.
- **How we calculate it**: We add up (`quantity` × `unit_price`) for all orders throughout a given month.
- **Where the data lives**: `orders`, `order_items`, and `products` tables.
- **Current Baseline**: We hit 5,086.50 JOD in June 2025.
- **Why we care**: It's the ultimate pulse-check for our business. Steady monthly growth proves that our market presence is actually expanding.

---

## KPI 2: Weekly Order Volume
- **Name**: Weekly Order Volume (Time-based)
- **What it is**: The exact number of successful orders placed each calendar week.
- **How we calculate it**: We just count the total number of non-cancelled `order_id`s per ISO calendar week.
- **Where the data lives**: `orders` table.
- **Current Baseline**: We're currently seeing about 3 to 6 orders per week.
- **Why we care**: This helps our operations team spot busy periods so we can plan staffing, load, and logistics around our peak trading days.

---

## KPI 3: Revenue by City
- **Name**: Revenue by City (Segmentation)
- **What it is**: A breakdown of how much money each location brings in.
- **How we calculate it**: Total revenue (`quantity` × `unit_price`) grouped by the customer's `city`.
- **Where the data lives**: `customers`, `orders`, `order_items`, and `products` tables.
- **Current Baseline**: Irbid sits at 7,250.50 JOD, though Amman leads the pack with over 15,700 JOD. 
- **Why we care**: It tells us exactly where we're winning geographically and where we should be running localized marketing campaigns.
- **The Stats Test**: We ran an independent T-test to see if folks in Amman actually spend more per cart than folks in Irbid. 
  - **The Result**: Not at all ($p = 0.936$). Customers in both cities share virtually identical spending habits per order—Amman just happens to have a much larger volume of customers.

---

## KPI 4: Average Order Value (AOV) by Category
- **Name**: AOV by Product Category (Segmentation)
- **What it is**: How much customers spend on average when buying from a specific kind of product line.
- **How we calculate it**: We figure out the total cost of each order, then average those totals across different categories.
- **Where the data lives**: `products` and `order_items` tables.
- **Current Baseline**: Electronics leads at roughly 52 JOD a pop, closely followed by Clothing at 48 JOD.
- **Why we care**: If we know which products naturally drive up cart values, we know exactly what to feature on the front page and in our ads.
- **The Stats Test**: We used a One-Way ANOVA to prove that these category differences aren't flukes.
  - **The Result**: It's highly significant ($p < 0.001$). The math guarantees that categories like Electronics and Clothing definitively drive naturally higher basket values than things like Food & Beverage. 

---

## KPI 5: Customer Lifetime Value (CLV) by Registration Cohort
- **Name**: CLV by Registration Cohort (Cohort-based)
- **What it is**: We group customers by the month they first signed up, then track how much money that specific "class" of users has spent with us over time.
- **How we calculate it**: The average total revenue generated per user, grouped by their `registration_date` month.
- **Where the data lives**: `customers`, `orders`, `order_items`, and `products` tables.
- **Current Baseline**: Early joiners (Nov/Dec 2024) have a much higher lifetime value (233-287 JOD) than recent signups.
- **Why we care**: It shows if we're naturally getting better at retaining users over time. If older cohorts maintain huge leads, it means our recent onboarding or retention efforts might be dropping the ball and need a second look.

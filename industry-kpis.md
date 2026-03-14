# Industry KPI Reference

Domain-specific metrics for 16 industries, organised by beginner / intermediate / advanced
dashboard scope. Sourced from Joy Ibe's 100+ Data Analytics Portfolio Projects guide.

---

## 1. Healthcare Analytics

**Beginner dashboards:** Patient admission trends, Disease case trends, Department performance, Patient demographics
- Bed occupancy rate, Average length of stay (ALOS), Patient admissions per day, Discharge rate, Patient age/gender split, Top diagnoses, Department utilisation %

**Intermediate dashboards:** Readmission rates, ER wait times, Cost by treatment, Staff workload
- 30-day readmission rate, ER wait time (median/90th percentile), Cost per patient episode, Staff-to-patient ratio, Overtime hours, Procedure volume vs capacity

**Advanced dashboards:** Readmission risk prediction, Bed demand forecasting, Disease spread, Fraud detection
- Predicted readmission probability score, Bed demand forecast vs actual, Reproduction number (R0), Anomalous billing patterns, Treatment outcome rates

**Domain rules:**
- Always split by ward/department — aggregated hospital data masks critical variation
- Include a capacity utilisation % — absolute numbers without capacity context mislead
- For disease dashboards: incidence rate per 1,000 population is more comparable than raw case counts

---

## 2. Sales & Retail Analytics

**Beginner dashboards:** Supermarket sales, Product category analysis, Seasonal trends, Store performance
- Total revenue, Units sold, Revenue per store, Revenue vs prior period %, Top 10 products by revenue, Sales by category, Day-of-week patterns

**Intermediate dashboards:** Customer segmentation, Discount impact, Stockout analysis, Returns
- RFM scores (Recency, Frequency, Monetary), Discount rate vs margin impact, Stockout frequency by SKU, Return rate %, Net promoter score

**Advanced dashboards:** Sales forecasting, Market basket analysis, CLV prediction, Dynamic pricing
- Forecast vs actual (MAPE), Association rules (lift, confidence), Customer lifetime value by segment, Price elasticity coefficient, Conversion rate by price band

**Domain rules:**
- Revenue without margin is vanity — always include gross margin % for retail
- Seasonality requires 12+ months of data before trends are meaningful
- Product-level analysis needs ABC classification (top 20% of SKUs = 80% of revenue)

---

## 3. Finance & Banking Analytics

**Beginner dashboards:** Credit card spending, ATM volumes, Loan approval trends
- Transaction volume, Average transaction value, Approval rate %, Declined transactions %, ATM utilisation rate

**Intermediate dashboards:** Loan default risk, Credit score segmentation, Retention, Branch profitability
- Default rate by product/segment, Non-performing loan (NPL) ratio, Probability of Default (PD), Customer retention rate, Net interest margin, Branch revenue per FTE

**Advanced dashboards:** Fraud detection, Credit risk, Portfolio risk, Market volatility
- Fraud detection rate, False positive rate, Credit risk score distribution, Value at Risk (VaR), Sharpe ratio, Portfolio beta

**Domain rules:**
- Always show ratios alongside absolutes — a £10M loan book and a 2% default rate tells a different story than the raw default count
- Time-lag metrics matter: loan defaults surface 3–6 months after origination
- Regulatory ratios (capital adequacy, liquidity coverage) belong in compliance dashboards, not performance

---

## 4. Telecommunications Analytics

**Beginner dashboards:** Usage trends, Data consumption, Call volume
- Data usage (GB/user), ARPU (Average Revenue Per User), Call minutes per user, SMS volume, Network uptime %

**Intermediate dashboards:** Churn analysis, Network usage by region, Plan upgrades
- Monthly churn rate, Churn by tenure cohort, Net Promoter Score, Plan upgrade rate, CSAT score, Data throttling events

**Advanced dashboards:** Churn prediction, Network traffic forecasting, Revenue optimisation
- Predicted churn probability, Days-to-churn estimate, Traffic forecast vs actual, Revenue per MHz (spectrum efficiency)

**Domain rules:**
- Churn rate = (customers lost in period) / (customers at start of period) — ensure consistent definition
- Distinguish voluntary churn (cancelled) from involuntary (payment failure) — interventions differ
- ARPU without COGS comparison misses profitability entirely

---

## 5. Logistics & Supply Chain Analytics

**Beginner dashboards:** Delivery time, Shipping cost by region, Order processing time
- On-time delivery rate (OTD), Average delivery days, Shipping cost per order, Orders processed per hour, Pending orders count

**Intermediate dashboards:** Supply chain delays, Inventory turnover, Supplier performance
- Delay rate by route/carrier, Inventory turnover ratio, Days of supply (DOS), Supplier on-time rate, PO fill rate, Damage rate

**Advanced dashboards:** Demand forecasting, Route optimisation, Supply chain risk
- Forecast accuracy (MAPE), Safety stock recommendation, Optimal route distance vs actual, Supplier risk score, Stockout probability

**Domain rules:**
- OTD = shipped on time AND delivered on time — conflating the two hides carrier failures
- Inventory turnover below industry benchmark signals cash tied up unnecessarily
- For Nigerian/African logistics context: factor fuel cost index and road condition ratings

---

## 6. E-commerce Analytics

**Beginner dashboards:** Website traffic, Purchase trends, Product page conversion
- Sessions, Bounce rate, Page views per session, Purchase conversion rate, Revenue per session

**Intermediate dashboards:** Customer journey funnel, Cart abandonment, Recommendation patterns
- Funnel drop-off rate per stage, Cart abandonment rate, Average order value (AOV), Cross-sell rate, Time to first purchase

**Advanced dashboards:** Recommendation system, CLV modelling, Personalised marketing
- Recommendation click-through rate, Customer lifetime value, Predicted next purchase date, Marketing attribution (last-touch vs data-driven)

---

## 7. Education Analytics

**Beginner dashboards:** Student performance, Course completion, Enrollment trends
- Average score by subject, Pass rate %, Completion rate, Enrollment by term, Attendance rate

**Intermediate dashboards:** Dropout risk, Course effectiveness, Online engagement
- Dropout rate by cohort, Pre/post assessment score delta, Time-on-platform per learner, Assignment completion rate

**Advanced dashboards:** Performance prediction, Admission forecasting, Learning outcomes
- Predicted final score, At-risk student probability, Admission conversion rate, Learning outcome achievement rate

---

## 8. Energy & Utilities Analytics

**Beginner dashboards:** Electricity consumption, Household usage, Renewable production
- kWh consumed per period, Peak demand hour, Renewable generation % of total, Grid reliability uptime

**Intermediate dashboards:** Demand by region, Power outage analysis, Billing trends
- Demand forecast vs actual (MW), Outage frequency, Mean time to restore (MTTR), Billing error rate

**Advanced dashboards:** Demand forecasting, Smart grid optimisation, Renewable prediction
- Load forecast accuracy, Grid efficiency %, Solar/wind capacity factor, CO2 intensity (kg/kWh)

---

## 9. Transportation & Mobility Analytics

**Beginner dashboards:** Public transport usage, Airline traffic, Taxi patterns
- Passenger boardings per route, Seat occupancy rate, Trip count by hour, Average fare

**Intermediate dashboards:** Traffic congestion, Rideshare demand, Flight delays
- Average journey time vs baseline, Delay rate %, On-time performance (OTP), Surge pricing frequency

**Advanced dashboards:** Traffic prediction, Dynamic pricing, Demand forecasting
- Traffic flow prediction MAPE, Revenue per available seat mile (RASM), Demand forecast vs actual

---

## 10. Marketing & Advertising Analytics

**Beginner dashboards:** Social media engagement, Email campaign, Website traffic
- Impressions, Reach, Engagement rate, Email open rate, Click-through rate (CTR), Unsubscribe rate

**Intermediate dashboards:** Channel attribution, Campaign ROI, Customer acquisition cost
- ROI by channel, Customer acquisition cost (CAC), Cost per lead (CPL), Attribution contribution % per channel

**Advanced dashboards:** Marketing mix modelling, Propensity modelling, Ad spend optimisation
- Incremental revenue per £ spend, Propensity score by segment, Marginal ROI by channel, Saturation curve

---

## 11. Agriculture & Agribusiness Analytics

*(Particularly relevant for emerging markets including Nigeria)*

**Beginner dashboards:** Crop yield trends, Farm production, Fertiliser usage
- Yield (tonnes/hectare) by crop/region, Input cost per hectare, Area under cultivation

**Intermediate dashboards:** Farm profitability, Crop price trends, Weather impact
- Gross margin per hectare, Price volatility index, Rainfall deviation from average, Yield vs weather correlation

**Advanced dashboards:** Yield prediction, Supply forecasting, Risk assessment
- Predicted yield vs actual, Price forecast accuracy, Climate risk score, Supply gap (forecast vs demand)

**Domain rules:**
- Always normalise yield by hectare — raw production numbers without area are misleading
- Price volatility is a key risk metric in agribusiness — include a rolling standard deviation
- Weather data integration is essential for causal analysis

---

## 12. Real Estate Analytics

**Beginner dashboards:** Housing price trends, Property sales, Rental comparison
- Median sale price, Price per sq metre, Days on market, Rental yield %, Inventory count

**Intermediate dashboards:** Investment ROI, Neighbourhood demand, Housing market trends
- Gross rental yield, Price-to-rent ratio, Absorption rate, Year-over-year price change %

**Advanced dashboards:** House price prediction, Investment forecasting, Valuation modelling
- Predicted price vs actual, Comparable sales adjustment score, Investment return forecast

---

## 13. HR & People Analytics

**Beginner dashboards:** Employee demographics, Attendance trends, Department distribution
- Headcount by department/location, Attendance rate, Gender/age distribution, Tenure distribution

**Intermediate dashboards:** Attrition analysis, Performance trends, Hiring pipeline
- Attrition rate, Voluntary vs involuntary split, Time-to-fill (days), Offer acceptance rate, Performance rating distribution

**Advanced dashboards:** Attrition prediction, Workforce demand forecasting, Compensation optimisation
- Attrition risk score, Workforce gap forecast, Pay equity ratio, Total compensation benchmarking

---

## 14. Sports Analytics

**Beginner dashboards:** Player performance stats, Team match performance, Tournament results
- Goals/assists/points per game, Win rate %, Average match score

**Intermediate dashboards:** Player efficiency, Team strategy, Injury patterns
- Player efficiency rating (PER), Possession %, xG (expected goals) vs actual, Injury frequency by position

**Advanced dashboards:** Performance prediction, Match outcome prediction, Recruitment analytics
- Predicted performance score, Win probability model, Player value above replacement (WAR)

---

## 15. Social Impact / NGO Analytics

**Beginner dashboards:** Donation trends, Volunteer participation, Program participation
- Total donations, Donor count, Average donation size, Volunteer hours, Program beneficiary count

**Intermediate dashboards:** Program impact evaluation, Fund allocation, Donor retention
- Cost per beneficiary, Program reach rate, Donor retention rate, Fund utilisation %

**Advanced dashboards:** Donation prediction, Impact forecasting, Aid distribution optimisation
- Predicted donation amount, Impact score per £ spent, Optimal aid allocation model

---

## 16. Government & Public Policy Analytics

**Beginner dashboards:** Population growth, Crime rate, Education enrollment
- Population growth rate, Crime incidents per 100,000, Enrollment rate, Literacy rate

**Intermediate dashboards:** Budget allocation, Crime patterns, Public health programs
- Budget variance %, Crime hotspot index, Program coverage rate, Cost per capita

**Advanced dashboards:** Crime prediction, Economic policy impact, Urban growth forecasting
- Crime risk score by area, Policy impact coefficient, Urban growth forecast vs actual

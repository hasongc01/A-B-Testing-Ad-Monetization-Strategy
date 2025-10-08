# Online Restaurant Reservations Product Ad Monetization Strategy

This project examines the effectiveness of sponsored ad layouts on RestaurantGrades, an online restaurant review platform operating as a two-sided digital marketplace. The analysis applies causal inference techniques to evaluate whether transitioning from the current ad design (linking to profile pages) to a new design (showcasing specific dishes) increases restaurant reservations, the platform’s North Star Metric.

A randomized controlled trial with three arms (Control, Current Ad, New Ad) is used to estimate average treatment effects (ATEs) through t-tests and regression models. Randomization is validated with balance checks, and a power analysis is conducted to assess precision. The study further explores heterogeneous treatment effects (HTE) across restaurant types (chain vs. independent, high vs. low rating) to evaluate scalability and external validity.

This work demonstrates applied skills in A/B testing, causal inference, experiment design, and product growth strategy, illustrating how data-driven insights can guide ad monetization decisions for digital marketplaces.

# Table of Contents
1. Business Context
2. Causal Question
3. Key Metrics
4. Experiment Design: Randomization Control & Balance Check, Precision & Power Analysis
5. Experiment Results: ATE, HTE
6. Conclusion & Further Improvements

# 1. Business Context 
## Business Model: Two-Sided Digital Marketplace
RestaurantGrades (RG) is an online restaurant review platform powered by user-generated content. It operates as a two-sided digital marketplace.
- Supply side: Restaurants seeking visibility and new customers.
- Demand side: Restaurant-goers searching for places to dine.

RG’s business model is heavily dependent on advertising revenue. The sales team sells sponsored listings at $300 per month, guaranteeing restaurants at least 1,000 impressions.

## Product Features
RG’s platform offers two main features
1. Profile Pages – Contain restaurant details (hours, contact info, reviews).
2. Search Page – Users search with filters; restaurants are displayed in organic and sponsored listings.
   
Sponsored Listings (Search Ads) 
- Sponsored results appear above organic results, similar to Google Search Ads.
- Currently, Ads are triggered when a user searches within 0.5 miles for a cuisine type.
- Example: A user searching for “Italian restaurants in Soho, NY” sees two Italian restaurants at the top of the results.

## New Ad Design Proposal
As part of the ad monetization growth strategy, RG is testing a new sponsored listing design.
The new ad design highlights specific dishes to spark user interest.
The data science team aims to measure ad effectiveness between the current and the new designs. 
If the new layout improves engagement based on the A/B testing, RG will scale it platform-wide.

# 2. Causal Question
The main goal of this experiment is to assess causal impact of sponsored ads across the platform.

Primary causal question: If RG switches from the current layout to the new layout, will reservations increase?

Secondary question: Does the current ad lift conversions vs without ads? 

Two Business Strategies can be developed from this experiment:
- If ads are impactful → increase subscription pricing via competitor analysis.
- If new ad design performs better → roll out platform-wide.


# 3. Key Metrics
## North Star / Primary Metric:
NSM: the number of bookings made directly through RG platform in a month.

- This metric is chosen because it is simple, business-aligned, scalable, and sensitive to experiments.
- This metric is analogous to other two sided digital marketplaces: rides booked (Uber) or nights booked (Airbnb).

## Secondary Metrics:
Secondary Metrics are phone calls and page visits.
- Phone Calls: The number of phone calls from the restaurant’s page in a month.
- Page Visits: The number of page visits to restaurant pages in a month.

These measure engagement and visibility, though reservations are the ultimate outcome.

# 4. Experiment Design

Randomization Control & Balance Check:

- Individual restaurants that do not currently subscribe to RG’s ads.

Treatment vs Control 
  - Treatment 1: Current ad layout
  - Treatment 2: New ad layout
  - Control: No ad

Check Experiment Design Notebook for details. 

Precision & Power Analysis:

- Accuracy: Unbiased estimates of ATE due to randomization.

- Bias: None, since assignment is random.

- Precision: Depends on variance of outcomes and sample size.

Check Experiment Design Notebook for details. 

# 5. Experiment Results

For Average Treatment Effect: 

Null Hypothesis (H₀)
- The average reservations per month in the treatment and control groups are equal

Alternative Hypothesis (H₁)
- Average reservations per month are different in treatment than in control

Check Experiment Result ATE Notebook for details


# 6. Conclusion


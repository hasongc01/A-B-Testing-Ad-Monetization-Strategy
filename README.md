# Online Restaurant Reservations Product Ad Monetization Strategy

This project examines the effectiveness of sponsored ad layouts on RestaurantGrades, an online restaurant review platform operating as a two-sided digital marketplace. The analysis applies causal inference techniques to evaluate whether transitioning from the current ad design (linking to profile pages) to a new design (showcasing specific dishes) increases restaurant reservations, the platform’s North Star Metric.

A randomized controlled trial with three arms (Control, Current Ad, New Ad) is used to estimate average treatment effects (ATEs) through t-tests and regression models. Randomization is validated with balance checks, and a power analysis is conducted to assess precision. The study further explores heterogeneous treatment effects (HTE) across restaurant types (chain vs. independent, high vs. low rating) to evaluate scalability and external validity.

This work demonstrates applied skills in A/B testing, causal inference, experiment design, and product growth strategy, illustrating how data-driven insights can guide ad monetization decisions for digital marketplaces.

# Table of Contents
1. Business Context
2. Causal Question
3. Key Metrics
4. Experimentation Goal
5. Randomization Control & Balance Check
6. Precision & Power Analysis
7. Hypothesis Testing
8. Experimental Results
9. Scale Up: Limitations, External Validity
10. Customer Segmentation: Heterogeneous Treatment Effects (HTE)
11. Further Improvements

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
- Ads are triggered when a user searches within 0.5 miles for a cuisine type.
- Example: A user searching for “Italian restaurants in Soho, NY” sees two Italian restaurants at the top of the results.

## Growth Strategy Proposal
As part of the ad monetization growth strategy, RG is testing a new sponsored listing design.
- Current design: Links to restaurant’s profile page.
- New design: Highlights specific dishes to spark user interest.
The data science team aims to measure ad effectiveness between these designs. If the new layout improves engagement, RG will scale it platform-wide.

# 2. Causal Question
If RG changes the ad layout from current to new design, will the number of restaurant reservations increase?

# 3. Key Metrics
## North Star / Primary Metric:
North Star Metric is the number of bookings made directly through RG platform in a month.

This metric is chosen because it is simple, business-aligned, scalable, and sensitive to experiments.

This metric is analogous to other two sided digital marketplaces: rides booked (Uber) or nights booked (Airbnb).

## Secondary Metrics:
Secondary Metrics are phone calls and page visits.
- The number of phone calls from the restaurant’s page in a month.
- The number of page visits to restaurant pages in a month.
These measure engagement and visibility, though reservations are the ultimate outcome.

# 4. Experimentation Goal
The main goal of this experiment is to assess causal impact of sponsored ads across the platform.

Two Business Strategies can be developed from this experiment:
- If ads are impactful → increase subscription pricing via competitor analysis.
- If new ad design performs better → roll out platform-wide.

# 5. Randomization Control & Balance Check
Randomization Unit
- Individual restaurants that do not currently subscribe to RG’s ads.

Treatment vs Control 
  - Treatment 1: Current ad layout
  - Treatment 2: New ad layout
  - Control: No ad

Method
- Complete random assignment, ~1,000 restaurants per group.

Balance Check
- Characteristics: star ratings, chain vs. independent.
- Method: Two-sample t-tests for covariate balance.
- Statistical significance → formal equivalence.
- Economic significance → practical equivalence (do differences matter for outcomes?).

# 6. Precision & Power Analysis
Accuracy: Unbiased estimates of ATE due to randomization.
Bias: None, since assignment is random.
Precision: Depends on variance of outcomes and sample size.

To improve power, we add control variables (stars, chain status) in regression to reduce residual variance.
This improves precision without biasing ATE estimates.

# 7. Hypothesis Testing

Null Hypothesis (H₀)
- The average reservations per month in the treatment and control groups are equal

Alternative Hypothesis (H₁)
- Average reservations per month are higher in treatment than in control

Statistical Method
- Two-sample t-test to estimate ATE (difference in mean reservations).
- One-sided test, since RG only cares about positive lift.

# 8. Experimental Results
The experiment results can be accessed from python notebook: 'ate_results.ipynb'

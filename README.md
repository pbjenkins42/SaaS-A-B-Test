# SaaS-A-B-Test

# Pricing A/B Test Analysis

## Overview

This project evaluates a pricing experiment conducted to determine whether increasing the price of a software product from **$39 to $59** leads to improved revenue performance. The experiment involved randomly assigning users to either the original price (control group) or the higher price (test group), with a 66% to 33% allocation respectively.

The analysis focuses on three key business questions:
1. Which price point should the company adopt ($39 or $59)?
2. What actionable insights can be derived to improve conversion rates?
3. Is the test duration sufficient, and when should the test be concluded?

---

## Data

Two datasets were used in the analysis:
- `test_results.csv`: Contains user-level test data including pricing assignment, conversion, source, device, and timestamp.
- `user_table.csv`: Contains user geographic data (city, country, latitude, longitude).

These datasets were joined on `user_id` for a complete view of user behavior and characteristics.

---

## Key Analysis Steps

- **Exploratory Data Analysis (EDA)**: Verified test/control split, checked price integrity, and explored user segments.
- **Conversion and Revenue Metrics**: Calculated conversion rate and revenue per user (RPU) across both groups.
- **Segmentation Analysis**: Examined performance by marketing source, device, and operating system to identify behavioral patterns.
- **Elasticity Modeling**: Estimated price sensitivity of different segments to guide targeted strategies.
- **Test Duration Analysis**: Evaluated statistical power and graphed weekly trends to assess result stability.

---

## Findings and Conclusions

- **Adopt the $59 Price Point**:  
  Although the test group ($59) had a slightly lower conversion rate, it consistently achieved a higher **revenue per user**, leading to greater overall revenue. The $59 price point is financially superior based on the observed data.

- **Segment-Based Insights**:  
  Certain segments—particularly **mobile users** and **SEO traffic**—exhibited higher price sensitivity. These findings suggest an opportunity to **personalize pricing or messaging** for these users to improve conversions without sacrificing revenue from less price-sensitive segments.

- **Test Duration is Sufficient**:  
  A power analysis confirmed that the experiment exceeded the sample size needed for statistically significant results. Furthermore, trend analyses of weekly **conversion rates and RPU** revealed stable, consistent behavior over time. There is no evidence of test drift or novelty effects, and the test can be confidently concluded.

---

## Final Recommendation

1. Roll out the **$59 price** across the entire user base.
2. Use behavioral segmentation insights to **target price-sensitive users** with tailored interventions.
3. **End the test** as it has reached statistical maturity and stability.

---

## Repository Structure

```
.
├── Pricing_A_B_Test.ipynb     # Main analysis notebook
├── test_results.csv           # Test group data
├── user_table.csv             # User demographic/location data
├── README.md                  # Project documentation (this file)
```

---

## Tools Used

- Python (Pandas, Matplotlib, Seaborn, Statsmodels)
- Jupyter Notebook
- Git/GitHub

---

## Future Work

- Deploy dynamic pricing or A/B targeting strategies based on observed segment sensitivities.
- Incorporate external data (e.g., session duration, referral quality) to enhance predictive modeling of conversion behavior.

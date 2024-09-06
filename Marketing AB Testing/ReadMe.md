# A/B Testing for Ad Campaign Effectiveness

## Project Overview

This project analyzes the effectiveness of marketing campaigns through **A/B testing**. The goal is to determine whether ad exposure results in higher conversion rates compared to a control group (PSA viewers). The analysis focuses on answering two key business questions:

1. **Would the campaign be successful?**
2. **How much of the success can be attributed to the ads?**

Using statistical analysis, including the **Mann-Whitney U Test** and **Chi-Square Test**, this project assesses the performance of the campaign, investigates the difference between the experimental (ad) and control (PSA) groups, and determines if these differences are statistically significant.

---

## Business Context

Marketing companies operate in a competitive environment where successful campaigns can drive significant business value. However, finding the right strategy requires data-driven decisions. A/B testing, a randomized experimentation process, allows businesses to compare different versions of marketing variables (e.g., web pages, banners, etc.) to see which performs better.

In this scenario, most users were exposed to ads (experimental group), while a smaller control group saw a **Public Service Announcement (PSA)** or nothing in the same space. The dataset collected from this experiment aims to analyze user behavior, conversion rates, and attribute the success (if any) to the ad campaigns.

---

## Data Dictionary

- **Index**: Row index
- **user_id**: Unique identifier for each user
- **test_group**: Group assignment: "ad" (exposed to ads) or "PSA" (control group exposed to PSA or nothing)
- **converted**: Whether the user purchased the product (True) or not (False)
- **total_ads**: Number of ads seen by the user
- **most_ads_day**: The day the user saw the highest number of ads
- **most_ads_hour**: The hour of the day the user saw the most ads

---

## Methodology

### 1. **Exploratory Data Analysis (EDA)**
   - Investigated the distributions of user behaviour in both test groups.
   - Visualized the conversion rates across various periods (day and hour).
   - Analyzed ad exposure and purchase behaviour trends.

### 2. **Statistical Tests**
   - **Mann-Whitney U Test**: Used to compare conversion rates between the ad and PSA groups. Since the data may not be normally distributed, this non-parametric test was chosen to assess whether there are significant differences in the ranks of conversion between the groups.
   - **Chi-Square Test**: Evaluated the statistical significance of categorical variables (converted vs. non-converted across test groups) to determine whether the differences in conversion rates are due to chance.

---

## Key Findings

1. **Conversion Rate Analysis**: Conversion rates were calculated and compared between the ad and PSA groups, showing how much the ads impacted user purchases.
2. **Statistical Significance**: The Mann-Whitney U and Chi-Square tests were performed to determine whether the difference in conversion rates between the ad and PSA groups was statistically significant.
3. **Impact of Ads**: This analysis quantified ad exposure's contribution to the campaign's overall success.

---

## Conclusion

This project highlights the importance of A/B testing in marketing strategy. Through the statistical analysis, the findings provide insights into how ad exposure influences customer behaviour, allowing businesses to make informed decisions on their advertising investments.

---

## Tools & Techniques

- **Python**: Data manipulation and analysis
- **Pandas**: Data wrangling
- **SciPy**: Statistical tests (Mann-Whitney U, Chi-Square)
- **Matplotlib/Seaborn**: Data visualization
- **Mann-Whitney U Test**: Non-parametric test for comparing conversion rates
- **Chi-Square Test**: Test of independence for categorical variables

---

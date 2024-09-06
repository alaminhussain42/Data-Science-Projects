# A/B Testing: Optimizing User Engagement Through Button Design

## Project Overview

This project focuses on improving user engagement within a mobile app by testing a critical element of the landing page: the **main action button**. We conducted an **A/B test** to compare the performance of the current button design (Control) with a newly designed version (Experimental) to determine which design yields a higher **Click-Through Rate (CTR)**.

---

## Business Objective

The key objective is to evaluate whether the new button design increases user engagement compared to the current design. User engagement is measured by **Click-Through Rate (CTR)**, which is the percentage of users who click the action button after landing on the page. Users were randomly assigned to two groups:

1. **Control Group**: Exposed to the current button design.
2. **Experimental Group**: Exposed to the newly designed button.

A successful outcome will guide a data-driven decision on whether to implement the new design across the app or keep the existing one.

---

## Business Hypothesis

We hypothesize that the new button design will lead to at least a **10% increase in CTR** compared to the existing button.

- **Null Hypothesis (H₀)**: There is no significant difference in CTR between the control group (current button) and the experimental group (new button).
- **Alternative Hypothesis (H₁)**: There is a significant difference in CTR between the control group and the experimental group, with the new button expected to perform better.

---

## Methodology

To test the hypothesis, we used a **Two-Sample Z-Test** to compare the CTR between the two groups. This test was chosen because it allows us to determine whether the difference in proportions (CTR) between two independent groups is statistically significant.

### Steps:
1. **Data Collection**: Gathered CTR data from users who interacted with either the control or experimental versions of the app.
2. **Exploratory Data Analysis (EDA)**: Visualized and summarized the CTR distributions for both groups.
3. **Statistical Testing**: Performed a **Two-Sample Z-Test** to test the null hypothesis. The z-test assumes that:
   - The data is normally distributed (or approximately normal for large sample sizes).
   - The samples are independent.
   - The sample size is large enough for reliable approximation using the z-distribution.
   
---

## Key Findings

1. **CTR Comparison**: The CTR was calculated for both the control and experimental groups.
2. **Z-Test Results**: The p-value from the z-test was used to assess whether the observed difference in CTR between the two groups was statistically significant.
3. **Decision**: If the p-value was below our significance threshold (alpha = 0.05), we rejected the null hypothesis, concluding that the new button design significantly improves CTR.

---

## Conclusion

The outcome of the two-sample z-test provides valuable insights into user behavior and engagement. If the test results are statistically significant, the company can confidently proceed with rolling out the new button design, knowing that it enhances user engagement.

---

## Tools & Techniques

- **Python**: For data analysis and statistical testing
- **Pandas**: For data wrangling and calculations
- **SciPy**: For performing the two-sample z-test
- **Matplotlib/Seaborn**: For data visualization
- **Two-Sample Z-Test**: To compare CTR between control and experimental groups

---


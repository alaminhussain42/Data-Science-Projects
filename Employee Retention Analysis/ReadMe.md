# Employee Retention Analysis

## Business Scenario and Problem

Company X's HR department aims to improve employee satisfaction and retention. With data collected from employees, the key question is: **What factors are likely to make an employee leave the company?** The goal is to build a predictive model to identify employees who are at risk of leaving, enabling the company to implement strategies to enhance employee retention.

## Dataset Overview

The dataset contains the following variables:

- **satisfaction_level**: Employee-reported job satisfaction level [0–1]
- **last_evaluation**: Score of employee's last performance review [0–1]
- **number_project**: Number of projects the employee contributes to
- **average_monthly_hours**: Average number of hours the employee worked per month
- **time_spend_company**: Duration the employee has been with the company (years)
- **Work_accident**: Whether the employee experienced a work accident
- **left**: Whether the employee left the company
- **promotion_last_5years**: Whether the employee was promoted in the last 5 years
- **Department**: The employee's department
- **salary**: The employee's salary (U.S. dollars)

## Summary of Model Results

### Logistic Regression

- **Precision**: 79%
- **Recall**: 82%
- **F1-Score**: 80%
- **Accuracy**: 82%

### Tree-Based Machine Learning

- **Random Forest Model**:
  - **AUC**: 96.7%
  - **Precision**: 85.3%
  - **Recall**: 88.6%
  - **F1-Score**: 86.9%
  - **Accuracy**: 95.6%

The Random Forest model outperformed the Decision Tree model.

## Conclusion and Recommendations

The analysis indicates that overwork is a significant factor contributing to employee dissatisfaction and turnover. Recommendations for improving employee retention include:

- **Limit Project Load**: Cap the number of projects employees can handle.
- **Promotions**: Consider promoting employees who have been with the company for at least four years or investigate dissatisfaction among these employees.
- **Work Hours**: Reassess expectations for work hours and consider rewarding or adjusting expectations based on hours worked.
- **Overtime Policies**: Ensure employees are aware of overtime pay policies and make expectations around workload and time off clear.
- **Work Culture**: Address and improve company-wide and team-specific work culture.
- **Evaluation Scales**: Implement proportionate reward scales based on effort and contributions.

## Next Steps

- **Data Leakage**: Investigate the impact of removing `last_evaluation` to ensure predictions are not biased. Explore if performance evaluations significantly influence employee retention.
- **K-Means Clustering**: Build and analyze K-Means clusters to gain additional insights into employee satisfaction and retention factors.

## Technologies Used

- **Programming Languages**: Python
- **Libraries**: Scikit-Learn, Pandas, NumPy
- **Models**: Logistic Regression, Random Forest



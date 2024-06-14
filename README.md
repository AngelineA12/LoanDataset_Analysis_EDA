# Loan Dataset Analysis Report

## Introduction

This report presents an analysis of a loan dataset aimed at identifying factors influencing loan default, with the goal of reducing credit losses for a leading online loan marketplace.

## Approach

### 1. Data Loading and Initial Exploration

The dataset was loaded and explored to understand its structure and initial characteristics.

### 2. Data Cleaning and Preparation

#### Handling Missing Values
Columns with more than 50% missing values were dropped, and missing data in remaining columns were imputed (numeric with median, non-numeric with mode).

#### Data Type Corrections
String percentages in 'int_rate' were converted to float format for analysis.

### 3. Exploratory Data Analysis (EDA)

EDA included visualizations to explore relationships and distributions:
- Histograms revealed a peak in loan amounts around $5,000-$10,000 post-cleaning, indicating a normal distribution.
- Boxplots showed that higher interest rates correlate with higher default rates, while lower rates are associated with higher fully paid rates.
- Loan status breakdown indicated a larger proportion of loans are fully paid compared to charged off, aligning with interest rate impact observations.
- Loan grade breakdown showed that Grade B loans are most prevalent.
- Term vs Loan Status plot revealed that 36-month terms are more popular, with balanced default rates compared to longer terms.
- Subgrade vs Loan Status plot highlighted:
  - Borrowers in A and B subgrades predominantly pay loans properly.
  - C subgrades show an equal split between paying and not paying.
  - D subgrades vary in loan performance.
  - E and F subgrades tend to have higher instances of not paying.
  - G subgrades show mixed performance across subcategories.

- Employment Length vs Loan Status plot indicated:
  - Longer employment length correlates with wider installment ranges, with some outliers.
  - Variability in installment payments exists across different employment lengths, notably around 7 years.

- Homeownership vs Loan Status plot showed:
  - Most borrowers are renters or have a mortgage.
  - Fewer borrowers own their homes.
  - Overall, homeownership status does not significantly impact loan payment behavior.

- Purpose vs Installment plot revealed:
  - Loans for house, small business, credit card, and debt consolidation have higher installment amounts.
  - Car and vacation loans have lower installment amounts.
  - Other purposes (home improvement, medical, education, wedding, renewable energy) show moderate installment amounts.

- Address State vs Loan Status plot highlighted:
  - Top states for loan issuance include California, New York, Texas, Florida, and New Jersey.
  - States with lower loan issuance include Montana, North Dakota, and Wyoming.

### 4. Correlation Analysis

Correlation with 'loan_status' highlighted significant variables:
- Factors positively correlated with default include higher interest rates ('int_rate'), sub-grade ('sub_grade'), and term length ('term').
- Negative correlations included recovery efforts ('recoveries', 'collection_recovery_fee') and payment amounts ('last_pymnt_amnt', 'total_pymnt_inv', 'total_pymnt').

### 5. Insights and Recommendations

#### Insights
- **Loan Amount Distribution**: Most loans fall within $5,000-$10,000, indicating a common borrowing pattern.
- **Interest Rates and Loan Status**: Higher interest rates are associated with higher default rates, underscoring the importance of interest rate setting in risk assessment.
- **Subgrade Analysis**: Subgrades A and B generally indicate lower risk, whereas lower subgrades (E, F) show higher default rates.
- **Employment Length**: Variability in installment payments suggests that longer employment history does not guarantee lower risk uniformly.
- **Homeownership and Purpose**: These variables have varying impacts on installment amounts but do not strongly influence loan repayment behavior uniformly.
- **Geographic Insights**: States with higher loan volumes may require targeted risk assessment strategies due to varied economic conditions and borrower profiles.

#### Recommendations
- **Risk Assessment**: Implement detailed risk models incorporating subgrade analysis, employment length insights, and geographic considerations.
- **Segmentation Strategy**: Tailor loan offerings based on purpose-specific risk profiles identified (e.g., higher risk associated with vacations versus debt consolidation).
- **Monitoring and Recovery**: Enhance monitoring and recovery strategies for loans with higher default probabilities, focusing on subgrades E and F.
- **Continuous Analysis**: Regularly update risk models based on emerging patterns in borrower behavior and economic conditions across states.
- **Enhanced Due Diligence**: Strengthen due diligence processes for states with higher loan issuance volumes, ensuring robust risk management.

#### Additional Recommendations Based on Graph Insights
- **Subgrade vs Loan Status**: Develop targeted risk assessment criteria for subgrades C, E, F, and G due to their varying performance.
- **Employment Length vs Loan Status**: Consider employment length as a factor in risk assessment, focusing on stability and income potential.
- **Purpose vs Installment**: Review loan terms and conditions based on purpose to align installment expectations with borrower capacity.
- **Homeownership vs Loan Status**: Explore homeowner status impact further through deeper segmentation or additional variables.
- **Address State Analysis**: Tailor risk models and lending strategies based on regional economic conditions and borrower demographics in high-volume states.

## Conclusion

This analysis provides actionable insights into the factors influencing loan default, guiding strategic decisions to mitigate credit losses effectively. By leveraging these insights and implementing recommended measures, the company can optimize risk assessment strategies and enhance loan portfolio performance.

---

This report synthesizes the methodology, findings, and recommendations from the loan dataset analysis, emphasizing the application of insights to reduce credit losses and improve risk management practices in lending operations.

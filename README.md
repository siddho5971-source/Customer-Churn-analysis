# Customer Churn Analysis

## Project Overview

An exploratory data analysis (EDA) project using Python to identify customer churn patterns, understand factors associated with customer attrition, and develop data-driven customer retention recommendations.

## Objectives

- Analyze overall customer churn and retention.
- Identify churn patterns across contract types, customer tenure, payment methods, and monthly charges.
- Visualize customer behavior using charts and summary statistics.
- Translate analytical findings into actionable business recommendations.

## Dataset

- **Source:** IBM Telco Customer Churn dataset
- **Records:** 7,043 customers
- **Features:** 21 columns
- **Target variable:** `Churn` — indicates whether a customer left the company.

The dataset contains customer demographics, subscribed services, contract information, billing details, tenure, and churn status.

## Tools & Technologies

- **Python** — data analysis
- **Pandas** — data manipulation and aggregation
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **Google Colab** — development environment

## Project Workflow

- **Data loading:** Imported the dataset and inspected its dimensions, columns, and sample records.
- **Data cleaning:** Checked for missing values and duplicate customer IDs. Blank `TotalCharges` values were handled by replacing them with zero after confirming that the affected 11 customers had zero tenure.
- **Exploratory data analysis:** Calculated churn metrics and compared churn across relevant customer groups.
- **Visualization:** Created charts to communicate churn distributions and customer behavior patterns.
- **Business insights:** Interpreted the results and proposed customer retention strategies.

## Key Results & Insights

### 1. Overall Customer Churn

- **Total customers analyzed:** 7,043
- **Customers who churned:** 1,869
- **Customers who stayed:** 5,174
- **Overall churn rate:** 26.54%

**Insight:** Approximately one in four customers in the dataset had churned, highlighting a potential customer retention challenge.

**Recommendation:** Monitor churn regularly and identify customer groups that may benefit from targeted retention efforts.

### 2. Churn by Contract Type

| Contract type | Total customers | Churned customers | Churn rate |
|---|---:|---:|---:|
| Month-to-month | 3,875 | 1,655 | 42.71% |
| One year | 1,473 | 166 | 11.27% |
| Two year | 1,695 | 48 | 2.83% |

**Insight:** Month-to-month customers have the highest churn rate, while two-year contract customers have the lowest.

**Recommendation:** Investigate the reasons for high churn among month-to-month customers. Consider appropriate loyalty benefits, longer-term contract incentives, and proactive customer support.

### 3. Churn by Customer Tenure

| Tenure group | Churn rate |
|---|---:|
| 0–12 months | 47.44% |
| 13–24 months | 28.71% |
| 25–48 months | 20.39% |
| 49–72 months | 9.51% |

**Insight:** Churn rates generally decline as customer tenure increases. Customers in their first year have the highest churn rate.

**Recommendation:** Strengthen onboarding, provide early customer support, and follow up proactively with new customers to address service issues before they leave.

### 4. Churn by Payment Method

| Payment method | Total customers | Churned customers | Churn rate |
|---|---:|---:|---:|
| Electronic check | 2,365 | 1,071 | 45.29% |
| Mailed check | 1,612 | 308 | 19.11% |
| Bank transfer (automatic) | 1,544 | 258 | 16.71% |
| Credit card (automatic) | 1,522 | 232 | 15.24% |

**Insight:** Customers using electronic checks have the highest churn rate, while customers using automatic credit card payments have the lowest.

**Recommendation:** Investigate whether billing experience, payment preferences, or other customer characteristics help explain this difference. Offer convenient payment options without assuming that payment method itself causes churn.

### 5. Monthly Charges by Churn Status

| Churn status | Average monthly charges | Median monthly charges | Customers |
|---|---:|---:|---:|
| Stayed | 61.27 | 64.43 | 5,174 |
| Churned | 74.44 | 79.65 | 1,869 |

**Insight:** Customers who churned had higher average and median monthly charges than customers who stayed.

**Recommendation:** Review pricing and service value for higher-paying customers. Explore whether suitable plans, transparent billing, or targeted support could improve retention.

*Note: Monthly charge values are reported in the dataset's original monetary units.*

## Visualizations

The project includes visualizations covering:

- Overall customer churn distribution
- Churn by contract type
- Churn by customer tenure
- Churn by payment method
- Monthly charges by churn status

These visualizations help compare customer groups and communicate the main findings clearly.

## Overall Conclusion

The analysis identified several customer segments associated with higher churn:

- Month-to-month contract customers had a churn rate of **42.71%**.
- Customers with 0–12 months of tenure had a churn rate of **47.44%**.
- Electronic-check customers had a churn rate of **45.29%**.
- Customers who churned had higher average monthly charges than those who stayed.

Together, these patterns suggest that early customer engagement, contract-related retention strategies, billing experience, and perceived service value are useful areas for further investigation.

The findings represent **associations, not proof of causation**. Further analysis would be needed to determine the reasons behind these patterns and evaluate which retention strategies are effective.

## Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory data analysis (EDA)
- KPI calculation and group-wise analysis
- Data visualization
- Interpretation of statistical summaries
- Business insight generation
- Communicating findings through a structured analytical report

## How to Run

1. Clone or download this repository.
2. Open the `.ipynb` notebook in Google Colab or Jupyter Notebook.
3. Ensure the required Python libraries are installed.
4. Make the dataset accessible using the path or URL specified in the notebook.
5. Run the notebook cells in order to reproduce the analysis and visualizations.

## Scope & Limitations

- This project focuses on descriptive analysis and visualization; it does not train a predictive machine-learning model.
- The results identify patterns in the available dataset and do not establish causal relationships.
- Retention recommendations should be tested against additional customer information and business outcomes before implementation.

---

**Project type:** Exploratory Data Analysis (EDA)  
**Dataset:** IBM Telco Customer Churn  
**Environment:** Google Colab

# Customer-and-Credit-Analytics

# Bank Credit Card Launch Strategy — Phase 1

## Project Overview

This project focuses on identifying potential target customers for AtliQo Bank's credit card launch by analysing customer demographics, credit profiles, and transaction behaviour.

Using Python and exploratory data analysis, the project examines customer income, age, credit scores, credit limits, outstanding debt, spending patterns, payment preferences, and shopping platforms to identify potentially underserved customer segments.

The objective is to provide data-driven recommendations for selecting a suitable target market for a trial credit card launch.

## Business Objectives

- Analyse customer demographics, including age, income, occupation, gender, and location.
- Clean and prepare customer, credit profile, and transaction datasets.
- Examine relationships between credit scores, credit limits, annual income, and outstanding debt.
- Understand customer spending patterns across product categories, payment methods, and shopping platforms.
- Identify customer segments with relatively low credit card usage.
- Recommend a potential target audience for AtliQo Bank's initial credit card launch.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data cleaning, transformation, merging, and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization and exploratory data analysis |
| MySQL | Database connectivity and data extraction |
| Jupyter Notebook | Interactive analysis and documentation |

## Project Structure

```
AtliQo-Bank-Credit-Card-Launch/
|
|-- phase_1_atliqo_bank.ipynb
|-- data/
|   |-- customers.csv
|   |-- credit_profiles.csv
|   |-- transactions.csv
|
|-- README.md
|-- requirements.txt

Note: Adjust the filenames and directory structure to match your actual project files. Include the data directory only if the datasets are available and you have permission to distribute them. 
```

## Datasets

The project analyses three primary datasets.

### 1. Customer Dataset

Contains customer demographic and financial information, including:

- Customer ID
- Age
- Annual income
- Occupation
- Gender
- Location
- Marital status

### 2. Credit Profile Dataset

Contains customer credit-related information, including:

- Customer ID
- Credit score
- Credit limit
- Outstanding debt

### 3. Transaction Dataset

Contains information about customer purchasing behaviour, including:

- Customer ID
- Transaction amount
- Payment method
- Shopping platform
- Product category

These datasets are used to examine relationships between customer characteristics, credit profiles, and purchasing behaviour.

## Project Workflow

### 1. Data Import

Imported customer, credit profile, and transaction data using CSV files or a MySQL database.

Loaded the datasets into Pandas DataFrames for further processing and analysis.

### 2. Customer Data Cleaning

Performed data quality checks on customer demographic and income information.

Key activities included:

- Identified missing annual income values and handled them using occupation-wise median income.
- Examined annual income distributions to identify unusually low income values.
- Investigated unusually low and high customer ages.
- Replaced selected anomalous income and age values using occupation-specific median values.
- Analysed customer demographics using statistical summaries and visualizations.

### 3. Credit Profile Analysis

Cleaned and analysed customer credit information to improve data quality.

Key activities included:

- Identified and removed duplicate credit profile records.
- Investigated missing credit limit values.
- Examined the relationship between credit scores and credit limits.
- Used credit score ranges and the most frequent credit limit within each range to impute missing values.
- Identified outstanding debt values exceeding credit limits and addressed them using the applicable credit limit as the replacement value.
- Analysed relationships among credit scores, credit limits, annual income, and outstanding debt.

### 4. Transaction Data Analysis

Examined transaction records to understand customer spending patterns and payment preferences.

Key activities included:

- Investigated missing shopping platform values and imputed them using the most frequently observed platform.
- Identified zero-value transactions and replaced them using median transaction amounts from relevant transaction groups.
- Investigated unusually high transaction amounts and treated outliers.
- Analysed payment method preferences across customer age groups.
- Compared product category preferences and shopping platforms.
- Examined average transaction amounts across customer segments.

### 5. Exploratory Data Analysis

Conducted exploratory analysis to understand customer characteristics and identify patterns relevant to credit card adoption.

The analysis examined:

- Customer age and income distributions.
- Credit score and credit limit distributions.
- Relationships between annual income and credit limits.
- Relationships between credit scores and credit limits.
- Outstanding debt relative to credit limits.
- Customer spending patterns across product categories.
- Payment preferences across different age groups.
- Shopping platform preferences among customer segments.

### 6. Customer Segmentation

Combined customer demographic information with credit profile and transaction data to analyse different customer segments.

Created age groups and compared their average annual income, credit scores, credit limits, and shopping behaviour.

The analysis also examined differences in credit card usage and purchasing preferences across age groups to identify potential opportunities for customer acquisition.

### 7. Target Market Identification

Evaluated customer segments to identify a potentially underserved market for AtliQo Bank's proposed credit card launch.

The analysis focused on younger customers who showed relatively low credit card usage and had lower average credit scores and credit limits than older customer groups.

## Key Findings

The following findings are documented in the notebook and should be interpreted in the context of the analysed dataset.

### 1. Young Adults Represent a Potential Market

- Customers aged 18–25 account for approximately 26% of the customer base in the analysed dataset.
- Their average annual income is below 50,000 in the dataset's monetary units.
- This group has relatively lower average credit scores and credit limits than some older customer groups.
- Their observed credit card usage is lower than that of other age groups.

These characteristics suggest that young adults could be a potential segment for further evaluation when designing a credit card product.

### 2. Relationship Between Credit Scores and Credit Limits

- Credit scores and credit limits exhibit a strong positive correlation of approximately 0.85 in the notebook's analysis.
- Annual income also shows a strong relationship with credit limits.
- Credit score ranges help explain differences in assigned credit limits.
- These relationships provide a basis for understanding customer credit profiles and handling missing credit limit values.

Correlation indicates an association between variables and does not, by itself, establish causation.

### 3. Customer Shopping Preferences

The analysis identifies the following prominent product categories among customers aged 18–25:

- Electronics
- Fashion and Apparel
- Beauty and Personal Care

Amazon, Flipkart, and Alibaba are identified as prominent shopping platforms in the analysed segment.

These observations can help inform potential customer acquisition campaigns and the selection of relevant shopping-related card benefits.

### 4. Data Quality Improvements

The project addresses multiple data quality issues across the datasets, including:

- Missing annual income values.
- Implausible customer ages.
- Duplicate credit profile records.
- Missing credit limits.
- Outstanding debt values exceeding credit limits.
- Missing shopping platform values.
- Zero-value transactions.
- Unusually high transaction amounts.

The cleaning process combines statistical analysis, group-based imputation, and business rules to prepare the data for further analysis.

## Business Recommendations

Based on the exploratory analysis, customers aged 18–25 represent a potential target segment for AtliQo Bank's trial credit card launch.

This segment accounts for approximately 26% of the analysed customer base and demonstrates relatively low credit card usage compared with older age groups.

AtliQo Bank could consider the following strategies:

- Develop an entry-level credit card designed for eligible young adults.
- Offer transparent fees and benefits aligned with customer spending behaviour.
- Explore rewards related to electronics, fashion, and personal care purchases.
- Evaluate digital acquisition campaigns across relevant shopping platforms.
- Apply responsible credit eligibility checks and affordability assessments.
- Conduct a pilot programme to evaluate customer interest and adoption before expanding the product.
- Monitor activation rates, transaction frequency, customer acquisition costs, and repayment behaviour.

These recommendations should be validated through additional analysis of customer eligibility, credit risk, profitability, and market demand before implementation.

## Getting Started

### Prerequisites

Install Python 3 and Jupyter Notebook, along with the libraries required for the analysis.

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
cd Customer-and-Credit-Analytics
```

### 2. Install Dependencies

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter mysql-connector-python
```

Alternatively, install the dependencies using the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### 3. Prepare the Dataset

Ensure that the required datasets are available and that the file paths in the notebook match their actual locations.

If the project uses CSV files, update the file paths accordingly.

If the project uses MySQL, configure the database connection using your own credentials and ensure that the required tables are available.

Never publish database passwords, API keys, or other sensitive credentials in a public repository.

### 4. Run the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `phase_1_atliqo_bank.ipynb` and execute the cells in sequence.

## Future Improvements

Potential extensions to the project include:

- Developing customer segmentation models to identify distinct customer groups.
- Building a credit risk assessment framework for prospective cardholders.
- Analysing customer profitability and expected credit card revenue.
- Estimating customer acquisition costs and potential return on investment.
- Creating an interactive Power BI dashboard to communicate findings.
- Designing a pilot programme or controlled experiment to validate the proposed target segment.
- Evaluating customer eligibility and affordability before recommending credit limits.
- Developing customer acquisition strategies based on spending behaviour and financial profiles.

## Conclusion

This project demonstrates how data cleaning, exploratory data analysis, and customer segmentation can support business decision-making in the banking sector.

By integrating customer demographics, credit profiles, and transaction behaviour, the analysis identifies young adults aged 18–25 as a potential underserved segment for AtliQo Bank's credit card launch.

The findings provide an initial direction for customer targeting and product development while highlighting the need for further credit risk, profitability, and market validation before implementation.

## Project Information

- **Project:** AtliQo Bank Credit Card Launch Strategy
- **Phase:** Phase 1 — Target Market Identification
- **Domain:** Banking and Financial Analytics
- **Focus Areas:** Data Cleaning, Exploratory Data Analysis, Customer Segmentation, Business Recommendations
- **Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, MySQL, Jupyter Notebook


# Motor Insurance Analytics Dashboard | Power BI

## Project Overview
This project analyzes motor insurance policy data using Microsoft Power BI.

The dashboard helps understand insurance policies, premium collections, claims paid, vehicle categories, and insurance portfolio performance.

The objective is to transform raw insurance data into meaningful insights using data cleaning, data modeling, DAX measures, and interactive visualizations.

## Tools & Technologies
- Microsoft Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Data Visualization
- Data Modeling

## Dataset
The dataset contains motor insurance information, including:

- Vehicle Type
- Vehicle Make
- Insurance Start Date
- Insurance End Date
- Premium Amount
- Insured Value
- Claim Amount
- Vehicle Usage
- Vehicle Production Year
- Vehicle Capacity

## Key KPIs
- Total Policies
- Total Premium
- Total Claims Paid
- Average Premium
- Average Claim
- Premium-to-Claim Ratio

## Dashboard Analysis
The dashboard explores:

- Insurance policy performance
- Premium collection analysis
- Claims paid analysis
- Vehicle type analysis
- Vehicle make analysis
- Policy opening and closing trends
- Premium-to-claim ratio
- Vehicle insurance portfolio analysis

## Data Preparation
Data preparation and transformation were performed using Power Query.

Steps included:
- Data cleaning
- Data type corrections
- Handling missing and incorrect values
- Date formatting
- Preparing data for analysis

## DAX Measures
DAX was used to create calculations and business metrics.

Examples:

### Total Policies
```DAX
Policy Count = COUNTROWS(policies)
```

### Total Premium
```DAX
Total Premium = SUM(policies[PREMIUM])
```

### Total Claims Paid
```DAX
Total Claims = SUM(policies[CLAIM_PAID])
```

### Policy Opened
```DAX
Policy opened = [Policy Count]
```

### Policy Closed
```DAX
Policy closed =
CALCULATE(
    [Policy Count],
    USERELATIONSHIP(
        'calendar'[Date],
        policies[INSR_END]
    )
)
```

## Business Insights
The dashboard supports analysis of:

- Which vehicle categories contribute the most policies?
- How much premium is collected?
- How much is paid towards claims?
- How does the premium-to-claim ratio vary across vehicle categories?
- How do policy opening and closing trends change over time?
- Which vehicle types contribute significantly to the insurance portfolio?

## Dashboard Preview

![Insurance Dashboard](Screenshots/dashboard.png)

## Project Files
- Power BI dashboard (.pbix)
- Dataset (if permitted to share)
- Dashboard screenshot

## Author
Data Analytics Portfolio Project


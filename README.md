# Marketing Strategy Analysis Project

---

## Project Overview
This project focuses on analyzing the impact of various marketing strategies and sales efforts on sales performance (measured as **"Amount Collected"**). Key objectives include:
- Identifying which strategies work best for different client types.
- Determining optimal resource allocation.

---

## Dataset Summary
The dataset includes metrics related to marketing campaigns and sales interactions. Key columns are:

- **Client Information**: `Client ID`, `Client Type`
- **Metrics**: `Number of Customers`, `Monthly Target`, `Amount Collected`, `Units Sold`
- **Marketing Campaigns**: Campaign via `Email`, `Flyer`, `Phone`
- **Sales Contacts**: Interactions (`Sales Contact 1-5`)
- **Competition Levels**: Number of competitors
- **Temporal Data**: `Calendardate`, derived `Calendar_Month`, and `Calendar_Year`

---

## Analysis Workflow

### 1. Data Quality & Preprocessing
- Data was loaded from `Campaign-Data.csv` and inspected for consistency.
- Date formatting was corrected, and temporal features were extracted.
- Null values were addressed, and feature engineering was performed.

### 2. Exploratory Data Analysis
- **Client Type Distribution**:
  - Large Facility (46%), Small Facility (28%), Medium Facility (17%), Private Facility (9%).
- **Correlation Analysis**:
  - Highest correlation with sales: `Unit Sold` (0.997), `Monthly Target` (0.608), and `Number of Customers` (0.607).
  - Marketing strategies varied in impact:
    - Flyers (0.44), Email (0.25), Phone (0.03).

### 3. Statistical Analysis
- **Multicollinearity**:
  - Evaluated using Variance Inflation Factor (VIF); all variables were suitable for regression.
- **OLS Regression**:
  - Significant variables included Campaign Flyer, Sales Contacts 1-4.
  - Model R-squared: **0.480**.

### 4. Impact of Marketing Strategies
- Results vary across client types: The values below explain the ROI on per dollar spent.
  - **Large Facilities**: 
    - Sales Contact 1 (**$11.7 ROI**), Sales Contact 4 (**$10.6 ROI**).
  - **Medium Facilities**: 
    - Campaign Flyer (**$4.1 ROI**), Sales Contact 2 (**$3.6 ROI**).
  - **Private Facilities**: 
    - Sales Contact 2 (**$6.6 ROI**).
  - **Small Facilities**: 
    - Limited impact; Sales Contact 2 had a minor positive effect (**$0.8 ROI**).

---

## Key Findings
1. **Effective Strategies by Account Type**:
   - Sales interactions drive higher returns than campaigns in most cases.
   - Flyers are particularly effective in Medium and Large Facilities.
2. **Strategy Synergies**:
   - Combining personal sales contacts with targeted campaigns (e.g., Flyers) enhances ROI.

---

## Recommendations
1. **Prioritize High-Impact Strategies**:
   - Increase investment in Sales Contacts, particularly Contacts 1, 2, and 4 for Large Facilities.
   - Leverage Campaign Flyers for Medium Facilities.
2. **Tailored Approaches**:
   - Adjust strategies for client types, focusing on their unique drivers of sales.
3. **Further Exploration**:
   - Examine synergies between Flyers and Sales Contacts.
   - Investigate reasons for weak impacts of Phone campaigns.

---

This README provides an overview of the project for replication or further exploration. For a detailed walkthrough of the analysis and code, refer to the provided notebook.

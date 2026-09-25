# Mega Market --- Sales & Profit Analytics Dashboard

## Project Overview

This project presents an end-to-end **Sales & Profit Analytics solution
for Mega Market**, a multi-category retail business operating across the
Delhi-NCR region.

The project demonstrates the complete analytics workflow:

**Client Requirements → Raw Data → Data Cleaning → Data Organization →
Analysis → Executive Dashboard → Quality Checks → Business Insights &
Recommendations**

The source workbook contains **2,002 raw transaction rows**, including
duplicate records and realistic data-quality issues. After cleaning and
validation, the analysis-ready dataset contains **2,000 transaction
rows**.

------------------------------------------------------------------------

## 1. Client Requirements & Business Problem

Mega Market operates a multi-category retail business selling products
across categories such as **Groceries, Household, Beverages, Personal
Care, Electronics, Snacks, and Stationery**.

The client provided a large transactional dataset containing realistic
data-quality challenges and required a complete analytics solution
covering:

-   Data cleaning and formatting
-   Data organization
-   Missing-value and duplicate checks
-   Net Sales calculation
-   Gross Profit calculation
-   Net Profit calculation
-   Profit margin analysis
-   Product and category performance
-   Monthly sales and profit trends
-   Customer and payment-method analysis
-   City contribution analysis
-   Returns analysis
-   Interactive dashboard
-   Key business insights
-   Actionable recommendations

### Client Requirements

![image alt](https://github.com/Soonatic/Mega-Market-Profit--Sales--Analysis/blob/845ea3ba67177173de38a83950573fafbd3603fd/Screenshot%202026-09-25%20150407.png)

  -----------------------------------------------------------------------
  Requirement                         Deliverable
  ----------------------------------- -----------------------------------
  **Data Cleaning**                   Remove exact duplicates,
                                      standardize text, handle missing
                                      values, normalize dates and numeric
                                      fields, and validate financial
                                      calculations.

  **Data Organization**               Build a structured, analysis-ready
                                      dataset with consistent columns and
                                      calculated metrics such as Net Qty,
                                      Net Sales, Gross Profit, and Net
                                      Profit.

  **Professional Formatting**         Apply date, number, percentage, and
                                      ₹ currency formats, filters, freeze
                                      panes, readable column widths, and
                                      useful conditional formatting.

  **Executive Dashboard**             Provide KPI cards, trend analysis,
                                      category/product analysis,
                                      customer/payment/city analysis,
                                      return analysis, and interactive
                                      filters.

  **Business Insights**               Identify sales drivers, weak
                                      performers, trend patterns, return
                                      issues, and customer/payment
                                      patterns.

  **Recommendations**                 Provide practical actions for
                                      inventory, promotions,
                                      merchandising, returns, discount
                                      strategy, customer retention, and
                                      data capture.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 2. Data Cleaning & Quality Assurance

The raw dataset contained **2,002 transaction rows**. The cleaning
process removed **2 exact duplicate rows**, resulting in **2,000 valid
transaction records**.

### Cleaning activities performed

-   Removed exact duplicate transaction rows
-   Standardized product and category text
-   Standardized Customer Type, Payment Method, and City values
-   Converted dates into a consistent Excel date format
-   Converted quantity fields into numeric values
-   Converted discount values into true percentage values
-   Applied ₹ currency formatting without visible decimal places
-   Validated Sales, Sales Return, Net Sales, COGS, Gross Profit, and
    Net Profit calculations
-   Validated quantity and return calculations
-   Preserved legitimate unknown values instead of guessing missing
    business information

### Data-quality results

  Quality Check                                  Result
  ------------------------------------- ---------------
  Original transaction rows                       2,002
  Exact duplicate rows removed                        2
  Final cleaned transaction rows                  2,000
  Financial calculation mismatches                    0
  Quantity / return validation issues                 0
  Date format                             `dd-mmm-yyyy`
  Currency format                              `₹#,##0`
  Discount format                                  `0%`

Blank Customer Type, Payment Method, and City values were retained as
**"Unknown"** rather than being artificially filled with guessed values.

![image alt](https://github.com/Soonatic/Mega-Market-Profit--Sales--Analysis/blob/336928d510d9b4e993cc2d50348ec004f58a755b/Screenshot%202026-09-25%20150438.png)

------------------------------------------------------------------------

## 3. Data Organization & Analytical Model

The cleaned dataset is structured as an Excel table named **`tblSales`**
and contains the following analytical fields:

-   Invoice ID
-   Date
-   Product
-   Category
-   Qty
-   Unit Price (₹)
-   Discount (%)
-   Sales (₹)
-   Return Qty
-   Sales Return (₹)
-   Net Qty
-   Net Sales (₹)
-   COGS (₹)
-   Gross Profit (₹)
-   Gross Profit Margin
-   Operating Expense (₹)
-   Net Profit (₹)
-   Net Profit Margin
-   Customer Type
-   Payment Method
-   City

### Key business calculations

**Net Qty**

`Qty − Return Qty`

**Net Sales**

`Sales − Sales Return`

**Gross Profit**

`Net Sales − COGS`

**Net Profit**

`Gross Profit − Operating Expense`

**Gross Profit Margin**

`Gross Profit ÷ Net Sales`

**Net Profit Margin**

`Net Profit ÷ Net Sales`

**Return Rate**

`Return Qty ÷ Qty`

These calculations create a consistent analytical layer for the
dashboard and business reporting.

------------------------------------------------------------------------

## 4. Executive Dashboard

The **Dashboard** sheet provides an executive-level view of Mega
Market's performance.

### Dashboard KPIs

-   Total Sales
-   Net Sales
-   Gross Profit
-   Net Profit
-   Total Quantity Sold
-   Net Quantity Sold
-   Average Order Value
-   Return Rate
-   Gross Profit Margin
-   Net Profit Margin
-   Sales Return Value

### Interactive filters

The dashboard includes dropdown-based filtering for:

-   Category
-   City
-   Customer Type
-   Payment Method
-   From Month
-   To Month

All major KPIs, charts, and analytical sections respond to the selected
filters through the **Calc** formula layer.

### Dashboard analysis areas

-   Monthly sales and profit trend
-   Category performance
-   Top and bottom products
-   City contribution
-   Customer Type mix
-   Payment Method mix
-   Return analysis
-   Live business highlights

------------------------------------------------------------------------

## 5. Key Business Insights

The full-year FY2025 cleaned dataset contains:

-   **Net Sales:** ₹779,939
-   **Gross Profit:** ₹202,290
-   **Net Profit:** ₹132,322
-   **Gross Profit Margin:** 25.9%
-   **Net Profit Margin:** 17.0%
-   **Gross Quantity:** 6,470 units
-   **Returned Quantity:** 114 units
-   **Net Quantity:** 6,356 units
-   **Return Rate:** 1.8%
-   **Cleaned Transactions:** 2,000

### Sales & Profit Drivers

**Groceries** is the largest category by Net Sales, contributing
approximately **38.3%** of full-year Net Sales. **Household** is the
second-largest category.

The strongest products by Net Sales include:

1.  Rice 5kg
2.  Wheat Flour 5kg
3.  Laundry Detergent 2kg
4.  Coffee 200g
5.  Shampoo 340ml

### Weak Performers

**Stationery** is the smallest category by Net Sales, while **Mineral
Water 1L** is the lowest-revenue product among products with recorded
sales.

### Monthly Trend

-   **August** is the peak month by Net Sales.
-   **February** is the weakest month by Net Sales.
-   Monthly performance varies throughout the year, making month-level
    monitoring useful for management reviews.

### Customer & Payment Mix

The dashboard compares customer segments including:

-   Member
-   Regular
-   New
-   Walk-in
-   Unknown

Payment analysis covers:

-   Card
-   Cash
-   UPI
-   Wallet
-   Unknown

City analysis covers:

-   Ghaziabad
-   Delhi
-   Noida
-   Gurugram
-   Unknown

### Returns

The overall return rate is approximately **1.8% of units**.
Category-level analysis is used to identify areas where return rates are
relatively higher and may require further investigation.

------------------------------------------------------------------------

## 6. Business Recommendations

Based on the cleaned data and dashboard analysis, the project provides
recommendations around:

-   Protecting inventory availability for high-performing products
-   Strengthening merchandising and promotional activity for weaker
    categories
-   Investigating categories with relatively high return rates
-   Improving checkout data capture for Customer Type, Payment Method,
    and City
-   Reviewing discount bands against both margin and sales volume
-   Monitoring Net Profit Margin monthly rather than relying only on
    annual totals
-   Using dashboard filters during business reviews to identify emerging
    category, city, product, or customer-level changes

------------------------------------------------------------------------

## 7. Workbook Structure

The Excel solution is organized into the following sheets:

  -----------------------------------------------------------------------
  Sheet                               Purpose
  ----------------------------------- -----------------------------------
  **Requirements**                    Documents client requirements,
                                      dashboard KPIs, analysis scope, and
                                      final deliverables.

  **Raw Data**                        Original transactional dataset
                                      before cleaning.

  **Cleaned Data**                    Validated and analysis-ready
                                      transaction table.

  **Dashboard**                       Executive Sales & Profit dashboard
                                      with interactive filters and visual
                                      analysis.

  **Insights & Recommendations**      Automated business insights and
                                      recommended actions.

  **Quality Checks**                  Cleaning summary and validation
                                      results.

  **Calc**                            Formula layer supporting dashboard
                                      calculations, live highlights, and
                                      reconciliation checks.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 8. Validation & Reconciliation

The project includes a dedicated **Quality Checks** sheet and a
formula-driven **Calc** layer.

The reconciliation checks confirm that major dashboard totals tie back
to the cleaned transaction data, including:

-   Net Sales
-   Category totals
-   Product totals
-   City totals
-   Customer Type totals
-   Payment Method totals
-   Invoice totals
-   Net Quantity totals
-   Net Sales = Total Sales − Sales Return

The final workbook reports successful reconciliation for the core
dashboard calculations.

------------------------------------------------------------------------

## 9. Tools & Techniques

### Tools

-   Microsoft Excel
-   Excel Tables
-   Excel formulas
-   Data validation / dropdown filters
-   Conditional formatting
-   Dashboard charts
-   Structured references
-   Named ranges
-   Formula-based analytical layer

### Analytics Techniques

-   Data cleaning
-   Duplicate detection
-   Missing-value handling
-   Data standardization
-   KPI development
-   Trend analysis
-   Category analysis
-   Product performance analysis
-   Customer segmentation
-   Payment-method analysis
-   Geographic analysis
-   Return-rate analysis
-   Profitability analysis
-   Reconciliation and quality assurance

------------------------------------------------------------------------

## 10. Project Outcome

This project transforms a large, messy retail transaction dataset into a
**professional, analysis-ready Sales & Profit Analytics solution**.

The final solution provides:

**Raw Data → Cleaned Data → Validated Metrics → Interactive Dashboard →
Business Insights → Actionable Recommendations**

It demonstrates practical skills in **Excel data cleaning, business
analytics, KPI development, dashboard design, financial calculations,
data validation, and management reporting**.

------------------------------------------------------------------------

## Repository Description

**End-to-end Mega Market Sales & Profit Analytics project featuring raw
and cleaned Excel data, an interactive executive dashboard, automated
KPI calculations, quality checks, business insights, and actionable
recommendations.**

------------------------------------------------------------------------

## Project Highlights

-   2,002 raw rows → 2,000 cleaned transactions
-   7 product categories
-   20 products
-   4 primary cities + Unknown
-   5 customer segments including Unknown
-   4 primary payment methods + Unknown
-   FY2025 monthly analysis
-   Sales, profit, margin, quantity, and returns KPIs
-   Interactive dashboard filters
-   Automated insights and recommendations
-   Formula-based reconciliation checks

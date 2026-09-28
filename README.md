# 📈 Business-Health-and-Customer-Behavior-in-2025

Dự án phân tích dữ liệu về sức khoẻ tài chính và hành vi khách hàng của doanh nghiệp Chứng khoán 2025
---
An end-to-end Business Intelligence project for a securities brokerage firm, transforming operational data into management insights across **business performance, customer retention, market liquidity, and margin activity**.

The project is designed as a **decision-support dashboard for management**, with the analysis moving beyond descriptive reporting to identify revenue concentration, KPI gaps, customer churn, trading behavior, and cash-flow movements.

---

## 📝 Project Objective

The objective is to build a centralized analytical view of brokerage operations by connecting data from multiple business areas, including:

- Customer profiles and account activity
- Securities transactions
- Revenue and business performance
- General ledger / financial movements
- Margin loans and margin revenue
- Portfolio / NAV information
- Market trading activity
- Business targets and planning data

The final Power BI solution helps management answer key questions such as:

- How is actual business performance tracking against targets?
- Which business units and revenue groups contribute most to revenue?
- Where is customer retention weakest?
- Which customer segments have higher churn or lower trading activity?
- How does company trading activity compare with overall market liquidity?
- Is customer cash flow showing net inflow or outflow?
- Which customer groups require closer retention or relationship management?

---

## 🗂️ Repository Structure

```text
├── 📁 data/
│   ├── Raw datasets
│   └── Processed datasets
│
├── 📁 Report/
│   ├── Report.pdf
│  
├── 📁 Power BI/
│   └── Securities_BI_Dashboard.pbix
│
├── 📁 dashboard/
│   └── Dashboard screenshots
│
└── README.md
```

> **Note:** Raw client and transaction data are not included in the public repository. Any displayed values are for analytical demonstration purposes.

---

## ⚙️ Data Pipeline & Analytical Workflow

### 1. Data Preparation & Transformation

Multiple operational tables were consolidated and prepared using **Power Query (M)**.

Key preparation activities included:

- Standardizing date and period formats
- Handling missing and null values
- Resolving inconsistent category mappings
- Cleaning customer and transaction identifiers
- Preparing business-unit and market mappings
- Creating analysis-ready dimensions and fact tables

The objective was to establish consistent business definitions before building the analytical model.

### 2. Data Modeling

A **Star Schema** was designed to connect transaction-level and planning-level data while maintaining appropriate granularity.

The model uses centralized dimensions such as:

- `Dim_Date`
- Customer
- Employee / Broker
- Business Division
- Securities / Ticker
- Market / Exchange

with corresponding fact tables covering:

- Transactions
- General Ledger
- Revenue / Fees
- NAV / Portfolio
- Margin
- Deposits & Withdrawals
- Market activity
- Business planning / targets

A centralized `Dim_Date` enables consistent time-based analysis across daily operational data and periodic target data.

### 3. DAX & Business Analytics

Power BI measures were developed to support management-level analysis, including:

- YTD / MTD performance
- Revenue and profit metrics
- KPI achievement against targets
- Revenue contribution and Pareto analysis
- Customer retention and churn rate
- Cohort retention analysis
- RFM customer segmentation
- NAV-based customer behavior
- Trading value and market share
- Net deposit / withdrawal flow
- Margin revenue and margin-related indicators

---

# 📊 Dashboard Overview

The project is organized around four analytical perspectives.

## 1. Business Performance & Revenue

Focuses on the overall financial performance of the brokerage business.

Key views include:

- Revenue, cost, profit and profit margin
- Actual vs. target performance
- Revenue contribution by business group
- Pareto analysis of revenue concentration
- Performance across divisions and business lines
- Margin revenue contribution

### Key management question

> Which business areas are generating revenue, and how does actual performance compare with the planned target?

---

## 2. Customer 360, Retention & RFM

Provides a customer-level view of account activity, retention and value.

Key analyses include:

- Active vs. inactive customers
- Overall churn rate
- Retention by customer cohort
- M3 retention by NAV segment
- Customer behavior by tenure and NAV
- RFM segmentation
- High-value customers with declining activity
- Customers with potential retention concerns

The RFM framework combines:

- **Recency** — how recently the customer traded
- **Frequency** — how frequently the customer traded
- **Monetary** — transaction/revenue value

The segmentation is used to distinguish customer groups requiring different relationship-management priorities rather than treating all customers equally.

### Key management question

> Which customers are generating value today, which customers are becoming inactive, and where should retention efforts be focused?

---

## 3. Market Liquidity & Trading Activity

Compares company-level trading activity with broader market conditions.

Key views include:

- Company trading value
- Total market trading value
- Trading market share
- Monthly liquidity trends
- Trading value by exchange
- Net deposits and withdrawals
- Cumulative cash-flow movement

This view helps separate changes in company activity from changes in the overall market environment.

### Key management question

> Is a change in company trading activity driven by market conditions or by changes in customer activity and capital flow?

---

## 4. Margin & Portfolio Analysis

Examines margin-related business performance together with customer asset and portfolio behavior.

Key analyses include:

- Margin revenue
- Margin outstanding
- Margin utilization
- NAV and portfolio structure
- Customer groups by asset level
- Profit / loss distribution
- High-value customer behavior
- Business opportunities associated with margin activity

### Key management question

> How does customer asset value translate into trading and margin business, and where are the key opportunities or areas requiring attention?

---

# 💡 Key Business Insights

### 1. Market Share Vulnerability

The analysis identified a decline in company market share during Q4 while overall market liquidity remained relatively substantial.

At the same time, the customer cash-flow analysis showed a negative net deposit/withdrawal position, indicating net capital outflow from the company during the analyzed period.

This creates a business question around whether the decline in trading activity is associated with changes in the company's customer base and capital availability rather than market liquidity alone.

---

### 2. Revenue Concentration & KPI Gap

The Pareto analysis shows a high concentration of actual revenue within the brokerage business.

Approximately **73% of total actual revenue** is attributed to the Brokerage division in the analyzed dataset, while the division's actual performance remains materially below its corresponding target.

This highlights the importance of monitoring both:

- Revenue contribution, and
- Distance to target

rather than evaluating business performance based on revenue size alone.

---

### 3. Customer Retention Is Most Challenging in the Early Lifecycle

The cohort analysis shows that customer retention declines substantially after account opening, with the most significant drop occurring during the early customer lifecycle.

This suggests that the **0–3 month period** is a critical stage for customer activation and retention.

The analysis therefore shifts the focus from simply measuring overall churn to identifying **when customers are most likely to become inactive**.

---

### 4. High-Value Customers Require a Different Retention Lens

NAV segmentation shows that customers with higher asset values do not necessarily have proportionally higher trading contribution.

For example, the **>5bn NAV segment** records relatively strong M3 retention while contributing a smaller share of customer activity.

This indicates that asset value and trading frequency should be evaluated together when assessing customer value.

A high-NAV customer with low trading frequency may represent a different business opportunity from a high-frequency, lower-NAV customer.

---

### 5. RFM Helps Prioritize Customer Management

The RFM analysis separates customers into different behavioral groups, including:

- Core / high-value customers
- Inactive or low-frequency customers
- Customers with potential value but declining activity
- Customers showing signs of churn

The analysis identified **35 customers in the high-value / potential-leaving group**, providing a specific customer pool for further review by the brokerage team.

---

# 📌 Selected KPI Snapshot

| KPI | Value |
|---|---:|
| Total Clients | 889 |
| Active Clients | 796 |
| Overall Churn Rate | 10.16% |
| Churn Rate – Lowest NAV Segment | 50.31% |
| Company Trading Value | 2.40M |
| Market Trading Value | 4.40M |
| Market Share | 0.05% |
| Net Deposit / Withdrawal | -1.65bn |
| Margin Revenue | 2.54bn |

> KPI values are based on the project dataset and are intended to demonstrate the analytical workflow. They should not be interpreted as current company performance.

---

# 🛠️ Tools & Technologies

- **Power BI** — Dashboarding, data modeling and business intelligence
- **Power Query / M** — Data cleaning and transformation
- **DAX** — KPI calculations, time intelligence, retention and segmentation
- **Excel** — Data preparation and validation
- **Star Schema** — Analytical data modeling
- **Cohort Analysis** — Customer retention analysis
- **RFM Analysis** — Customer value and behavior segmentation
- **Pareto Analysis** — Revenue concentration analysis

---

# 🚀 How to Use

1. Clone the repository.

```bash
git clone <repository-url>
```

2. Open the Power BI file:

```text
dashboards/Securities_BI_Dashboard.pbix
```

3. If Power BI requests a data source, update the source path to the corresponding files in:

```text
data/
```

4. Refresh the model and interact with the dashboard using the available filters for:

- Year / period
- Customer segment
- NAV group
- Business division
- Broker / employee
- Market / exchange

---

# 🎯 Project Outcome

This project demonstrates how fragmented brokerage data can be transformed into a **management-oriented BI solution**.

Instead of reporting isolated KPIs, the dashboard connects:

**Business Performance → Customer Behavior → Capital Flow → Market Conditions → Business Opportunities**

The resulting analysis provides a framework for management to monitor performance, identify customer-retention issues, understand revenue concentration, and investigate changes in trading activity.

---

## 👤 Project Focus

**Role:** Data Analyst / Business Intelligence Analyst

**Primary focus:** Business analysis, customer analytics, KPI monitoring, dashboard storytelling and decision-support insights.

**Domain:** Securities Brokerage / Financial Services

**Tools:** Power BI · Power Query · DAX · Excel

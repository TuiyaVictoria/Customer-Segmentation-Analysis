# Customer Segmentation using RFM Analysis
This project performs customer segmentation using RFM (Recency, Frequency, Monetary) analysis on transactional retail data.
The goal is to identify high-value customers, customers at risk of churn, and low-value segments to support data-driven marketing and retention strategies.
### Business Problem
Retail businesses often struggle to:
Identify their most valuable customers
Detect customers likely to churn
Allocate marketing resources effectively

Using historical transaction data, this project segments customers based on purchase behavior to answer:
Who are our best customers?
Which customers are at risk?
Where should the business focus retention efforts?

### Dataset
Online Retail Dataset
Source: Kaggle

### Key Columns
InvoiceNo
StockCode
Description
Quantity
UnitPrice
InvoiceDate
CustomerID
Country

### Data Cleaning Steps
Removed records with null CustomerID
Excluded canceled transactions (InvoiceNo starting with 'C')
Filtered negative quantities and prices
Created a revenue column (Quantity × UnitPrice)

### RFM Metrics Definition

| Metric        | Description                |
| ------------- | -------------------------- |
| **Recency**   | Days since last purchase   |
| **Frequency** | Number of unique purchases |
| **Monetary**  | Total revenue per customer |

### Customer Segmentation Logic
Customers were grouped into business-friendly segments:
| Segment             | Description                      |
| ------------------- | -------------------------------- |
| Champions           | Recent, frequent, high spenders  |
| Loyal Customers     | Consistent purchasers            |
| Potential Loyalists | Recent but less frequent         |
| At Risk             | Previously valuable but inactive |
| Lost                | Low activity and low spend       |

### Key Insights
A small percentage of customers (“Champions”) generated a disproportionate share of total revenue
“At Risk” customers showed high historical spend but long inactivity periods
“Lost” customers contributed minimal revenue and required low-priority marketing spend
### Business Recommendations
Champions: Loyalty programs, early access, exclusive offers
Loyal Customers: Cross-sell and upsell campaigns
At Risk: Win-back discounts and targeted re-engagement
Lost: Minimal spend or automated reactivation

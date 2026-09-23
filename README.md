# E-Commerce Sales Data Cleaning & Automated Financial Reporting

An automated Python data pipeline designed to clean raw e-commerce transaction logs, eliminate operational anomalies, and generate structured financial performance summaries.

## 📌 Business Problem
A client operating an e-commerce store provided raw sales records containing critical data quality issues:
- **Duplicate Records:** Inadvertently duplicated transactions artificially inflating order counts.
- **Missing Information:** Incomplete entries with absent product titles and missing unit counts.
- **Anomalous Values:** Physically impossible negative quantities corrupting total revenue calculations.

The objective was to sanitize the transaction history and output a clear, actionable Excel report summarizing sales volumes and total revenue grouped by product.

## 🛠 Tech Stack
- **Language:** Python
- **Libraries:** Pandas, OpenPyXL
- **Environment:** Google Colab / Jupyter

## ⚙️ Solution Architecture & Pipeline
1. **Deduplication:** Identified and purged identical transaction rows using `drop_duplicates()`.
2. **Missing & Invalid Data Filtering:** Handled null values (`dropna`) across critical columns and filtered out invalid transactions (`Adet > 0`).
3. **Revenue Modeling:** Computed line-item totals (`Quantity * Unit Price`) and generated aggregated metrics (`groupby`, `agg`) per product.
4. **Automated Export:** Transformed the analytical summary into a stakeholder-ready Excel spreadsheet (`to_excel`).

## 📊 Sample Output
| Ürün Adı | Toplam Satış Adedi | Toplam Ciro (TL) |
| :--- | :--- | :--- |
| **Klavye** | 3 | 2,550 |
| **Kulaklık** | 3 | 1,350 |
| **Mouse** | 3 | 900 |

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/EnverKangal/ecommerce-sales-data-cleaning.git](https://github.com/KULLANICI_ADIN/ecommerce-sales-data-cleaning.git)

# Customer Segmentation & Revenue Insights — Python + Power BI

## 🎯 Executive Project Summary
An enterprise-grade customer behavioral analytics system engineered to track customer lifetime value (CLV), purchase velocity, and retention risk. By deploying a hybrid methodology combining raw statistical processing in **Python** with advanced **Power BI** relational modeling, this project transforms over 5,000 transaction logs into a highly actionable corporate retention studio.

* **The Core Insight:** A custom Pareto analysis revealed that the top **21% of high-value spenders drive roughly ~65% of the total corporate revenue portfolio**, proving extreme financial concentration.

---

## Data Engineering & Modeling (Python Layer)
Instead of relying on rigid, flat database summaries, a custom analytical data engineering pipeline was built in Python (Pandas/NumPy) to group transactional data by customer ID:
* **Recency Metric:** Calculated the precise number of operational days since each customer's last distinct purchase occasion.
* **Frequency/Monetary Scoring:** Built statistical **RFM Quintile Models** using Pandas `qcut` data binning to assign relative 1-5 behavior rank tiers to every customer record.
* **Pareto Concentration:** Scripted a running cumulative sum percentage tracker to map out high-value revenue clusters.
* **Data Synthesis:** Merged the new multidimensional customer metrics back into the core granular transaction table via an optimized relational merge, exporting an enriched dataset for interactive slicing.

---

## Business Intelligence Architecture (Power BI Layer)
The interactive studio is built across 3 distinct, cohesive pages designed with a strict corporate layout template (Corporate Navy `#1B365D` on a Light Slate canvas):

### Page 1: Customer Portfolio Health Matrix
* **Diagnostic Panel:** Features a dark vertical sidebar tracking macro capitalization (`Total Revenue`, `Unique Orders`, `Average Order Value`) calculated using explicit, performance-optimized DAX measures.
* **Hero 5x5 Behavioral Heatmap:** A customized cross-tab matrix tracking `Recency` vs `Frequency` score tiers, utilizing background color gradients to spotlight exactly where cash flow is concentrated.
* **Pareto Curve:** A dual-axis Line and Column visual mapping individual customer revenue ranks against a cumulative percentage curve ending at 100% with zero layout scrollbars.

### Page 2: Churn Risk & Retention Command
* **Financial Exposure Hook:** Evaluates total `Revenue at Risk` and `Portfolio Churn Rate` via specialized DAX conditional metrics.
* **Revenue Exposure Scatter Plot:** Clusters customers spatially across an executive grid (Days Inactive vs Total Sales) to instantly isolate high-value accounts sliding into the inactive zone.
* **Actionable Churn Hit-List:** A highly filtered operational ledger supplying account managers with the exact names, states, and primary product lines of leaking accounts for direct outreach.

### Page 3: Deep-Dive Customer Explorer
* **Dossier Search Engine:** Employs an interactive lookup index to load an individual customer’s complete history.
* **Purchase Velocity Timeline:** A smooth Bezier curved line visual illustrating lifecycle spending trends.
* **Collapsible Transaction Ledger:** A multi-dimensional cross-tab matrix splitting specific orders by category with active horizontal data bars to analyze granular line-item invoices.

---

## How to Run the Project
1. Clone this repository or download the files.
2. Run the `Customer_Segmentation_Model.ipynb` file inside Anaconda/Jupyter Notebook to review the statistical modeling engine.
3. Open `Superstore_Customer_Segmentation_RFM.pbix` in Power BI Desktop to interact with the full live studio.

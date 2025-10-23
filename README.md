
## 🛋️ E-commerce Furniture Sales & Discount Analysis

### 📘 Project Overview

This project analyzes a **2,000-row AliExpress furniture dataset** to uncover how **product attributes, pricing, discounts, and shipping tags** influence sales performance. The goal is to identify key sales drivers, visualize pricing dynamics, and provide actionable insights for merchandising and business strategy.

### 🧾 Dataset Summary

* **Source:** AliExpress (scraped dataset)
* **Records:** 2,000 products
* **Period:** Snapshot dataset (2024)
* **Key Columns:**

  * `productTitle` – Product name (text)
  * `price` – Current selling price
  * `originalPrice` – Original listing price (≈75% missing)
  * `sold` – Units sold (target variable)
  * `tagText` – Shipping/promotion tag (e.g., *Free shipping*)

### ⚙️ Tools & Techniques

* **Tools:** Power BI, Python, Pandas, Seaborn, Matplotlib
* **Data Cleaning:** Removal of currency symbols, missing-value handling, feature engineering
* **Feature Engineering:**

  * `discount_pct` = (originalPrice − price) / originalPrice
  * `is_free_shipping` (binary feature)
  * `log_price`, `price_bin`, and keyword extraction from product titles
* **Modeling Approaches:** Linear Regression & Random Forest (with log-target transformation)

### 📊 Dashboard Highlights

#### Page 1 – Overview

* KPIs: Total Units Sold, Average Price, Median Sales
* Top 10 Products by Sales
* Price Distribution Histogram
* Average Sales by Price Range

#### Page 2 – Pricing Analysis

* Price vs Sold Scatter Plot
* Discount vs Sales Column Chart
* Correlation Matrix (Price, Discount, Sales)

#### Page 3 – Shipping & Tags

* Tag Distribution (Free vs Paid Shipping)
* Average Sales by Shipping Type
* Keyword Treemap (“sofa”, “chair”, “wooden”, etc.)

### 🔍 Key Insights

* **Free shipping** dominates (~90%) and slightly boosts sales.
* **Lower-priced products (<$30)** sell the most units → high price sensitivity.
* **Discounted items** (>20%) generally perform better but show wide variance.
* **Product titles** with keywords like *sofa*, *chair*, or *set* correlate with higher sales.
* Some **high-priced items** achieve strong sales → brand/design influence.

### 💡 Strategic Recommendations

* **Pricing:** Focus promotions on mid-range price bins with highest elasticity.
* **Tags:** Introduce diverse tag strategies (e.g., “Bundle Offer”, “Flash Deal”).
* **Inventory:** Maintain stock of top-performing SKUs; cross-sell via title keywords.
* **Modeling:** Combine cleaned numeric, discount, and text-based features for predictive analysis.

### 🧮 Conclusion

Price remains a crucial but **not exclusive** determinant of sales — product presentation, keyword usage, and free shipping also play significant roles.
This analysis demonstrates how **data-driven insights** can enhance product strategy, optimize pricing, and improve conversion in e-commerce.

Would you like me to make a **shorter GitHub-style version** (under 300 words, with emojis and badges like “📈 Built with Power BI & Python”) for your repository’s `README.md`?

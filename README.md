# 📊 Dynamic Retail Dashboard in Excel

## 🧩 Overview

The aim of this project is to build a detailed and interactive dashboard tailored for retail data analysis. Utilizing key performance indicators (KPIs) and compelling visualizations, the dashboard uncovers insights related to sales trends, profitability, product performance, and return patterns. It serves as a strategic tool to help retail managers and stakeholders make informed, data-backed decisions through a clear and engaging interface.

---

## 📚 Datasets Used

### 1. Orders Table
Contains detailed records of customer orders, including:
- Product, shipping, and customer information
- Financial metrics (Sales, Profit, Discount)
- Market and segment details

**Sample:**

| Order ID       | Returned | Order Date | Ship Mode   | Customer Name | Segment   | Country       | Market | Sales   | Profit  | Discount |
|----------------|----------|------------|-------------|----------------|-----------|---------------|--------|---------|---------|----------|
| CA-2012-124891 | No       | 31-07-2020 | Same Day    | Rick Hansen    | Consumer  | United States | US     | 2309.65 | 762.18  | 0        |
| IN-2013-77878  | Yes      | 05-02-2021 | Second Class| Justin Ritter  | Corporate | Australia     | APAC   | 3709.40 | -288.77 | 0.1      |

---

### 2. Returns Table
Captures details of returned orders by market.

**Sample:**

| Returned | Order ID        | Market  |
|----------|------------------|---------|
| Yes      | MX-2013-168137   | LATAM   |
| Yes      | US-2011-165316   | LATAM   |
| Yes      | ES-2013-1525878  | EU      |

---

### 3. People Table
Includes sales representatives and their regional assignments.

**Sample:**

| Person           | Region   |
|------------------|----------|
| Anna Andreadi    | Central  |
| Chuck Magee      | South    |
| Deborah Brumfield| Africa   |

---

## 💡 Problem Statements Solved with Implementation Steps

### ✅ 1. KPI Calculation
**Goal:** Dynamically calculate Total Sales, Profit, Quantity, Orders, and Profit Margin.

**Steps:**
- Load data using Power Query
- Create calculated fields:
  - `Profit Margin = Profit / Sales`
- Use Pivot Table With 'Sales','Profit','Quantity','OrderID','Profit Margin' in values.
- Build a KPI summary table using icons for visual clarity (💰, 📦, 📈)

![kpi](https://github.com/user-attachments/assets/b4cece2b-c8da-45c3-90fb-d105133091df)

---

### 📈 2. Sales and Profit Analysis
**Goal:** Visualize sales and profit relationship.

**Steps:**
- Use Scatter Plot to show the relation between Sales and Profit.
- Add `Sales` to X Value and `Profit` Y to values

![Screenshot 2025-07-02 130055](https://github.com/user-attachments/assets/8d65bb2b-bfee-4990-83d4-b935f749ffdf)

---

### 📊 3. Category-Wise Profit
**Goal:** Identify the most profitable product categories.

**Steps:**
- Pivot Table with `Category` as rows and `Profit` as values.
- Add Pie Chart for visual representation
- Also Included all the Kpi as values so that, if you want category wise sales then we can find it.
- created a seperate table for category and fill the all the values of kpi dynamically.
- Add filters for deeper analysis.

![Category](https://github.com/user-attachments/assets/c1caa770-7edd-4323-9c7b-de37a760a2c5)

---

### 🧭 4. Segment-Wise Profit Share (%)
**Goal:** Show sales contribution per customer segment.

**Steps:**
- Pivot Table with `Segment` as rows and `Profit` as values
- Use formula: `Segment Profit / Total Profit * 100`
- Display via Pie or Donut Chart with percentage labels

![Screenshot 2025-07-02 125825](https://github.com/user-attachments/assets/2f7f3113-acb3-4631-86a7-0de98c54934a)

---

### 🌍 5. Country-wise Profit
**Goal:** Analyze geographic Profit distribution.

**Steps:**
- Pivot Table with `Country` and `Profit`
- Use conditional formatting or create a Map Chart
- Highlight top-Profit making countries

![Screenshot 2025-07-02 125941](https://github.com/user-attachments/assets/c43f39b8-896c-49d5-8243-ade665708173)

---

### 🥇 6. Top 5 Subcategories
**Goal:** Discover the best-performing subcategories.

**Steps:**
- Pivot Table: `Sub-Category` + `Sales`
- Sort in descending order
- Filter Top 5 only
- Column Chart for visualization

![Screenshot 2025-07-02 130352](https://github.com/user-attachments/assets/27a759a7-05d1-4933-94af-289deb35b995)

---

### 🚫 7. Bottom 5 Subcategories
**Goal:** Highlight underperforming subcategories.

**Steps:**
- Similar to above but sort in ascending order
- Filter Bottom 5 only
- Use Bar chart for visualization

![Screenshot 2025-07-02 130441](https://github.com/user-attachments/assets/025fc07b-76b0-4a94-a09c-b013a7d6f435)

---

### 📆 8. Yearly Sales Trends
**Goal:** Track performance across years.

**Steps:**
- Group `Order Date` by Year/Month
- Add `Sales` to values
- use Sparklines for trend overview
- Use slicers for category/region/segment filtering

![Screenshot 2025-07-02 130539](https://github.com/user-attachments/assets/d96b8e31-0b26-4777-87e6-267f1b0309db)

---

## 🔄 Next Steps / Extensions

Enhance dashboard insights with:
- **Return Analysis:** Spot patterns by category and region
- **Top & Bottom Customers:** Identify loyal and risky customers
- **Market Comparison:** Evaluate different regional performances
- **Product-Level Insights:** Drill down into product contribution

---

## 🧠 Why This Dashboard Matters

This Excel-based solution helps retail stakeholders to:
- Monitor performance using clear KPIs
- Identify profitable areas and improvement zones
- Understand customer, category, and market dynamics
- Make informed, strategic business decisions with ease

---

## 📌 Tools Used
- Microsoft Excel
- Power Query Editor
- Pivot Tables & Charts
- Conditional Formatting & Slicers

---

## 📎 Visuals
This repository includes:

- Visual examples for each solved problem statement.
- Snapshots of the final dashboard with all components.

![Dashboard_img](https://github.com/user-attachments/assets/e41d8a75-7520-4429-9a9e-8500809bd8eb)

---

## 📬 Few Insights from Dashboard
- The APAC market reports the highest sales, primarily driven by the Technology category, with Phones being the leading sub-category.
- Within the APAC region, India emerges as the top-performing country in terms of sales.
- Despite having lower overall sales, the Canadian market demonstrates the highest profitability among all regions.
- There is a positive correlation between sales and profit — as sales increase, profit also tends to increase.
- In the LATAM market, the Binders product category has the highest return rate, with 7.98% of orders being returned.
---


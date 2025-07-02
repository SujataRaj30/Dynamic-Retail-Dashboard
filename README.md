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
  - `Order Count = COUNT(Order ID)`
- Use Excel formulas:
  - `=SUM(Sales)` for Total Sales
  - `=SUM(Profit)` for Total Profit
  - `=SUM(Quantity)` for Total Quantity
- Build a KPI summary table using icons for visual clarity (💰, 📦, 📈)

![kpi](https://github.com/user-attachments/assets/b4cece2b-c8da-45c3-90fb-d105133091df)

---

### 📈 2. Sales and Profit Trend Analysis
**Goal:** Visualize sales and profit movement over time.

**Steps:**
- Pivot Table with `Order Date` (Grouped by Month/Year)
- Add `Sales` and `Profit` to values
- Line Chart to show trends
- Add slicers for filters (e.g., Region, Segment)

![Sales vs Profit](https://github.com/user-attachments/assets/0ed77c31-5290-47b5-a5c0-87fad407a03b)

---

### 📊 3. Category-Wise Profit
**Goal:** Identify the most profitable product categories.

**Steps:**
- Pivot Table with `Category` as rows and `Profit` as values
- Sort by Profit descending
- Bar Chart for visual representation
- Add filters for deeper analysis

![category](https://github.com/user-attachments/assets/d4558765-f017-4a7c-9d81-a5d184a8f040)

---

### 🧭 4. Segment-Wise Sales Share (%)
**Goal:** Show sales contribution per customer segment.

**Steps:**
- Pivot Table with `Segment` as rows and `Sales` as values
- Use formula: `Segment Sales / Total Sales * 100`
- Display via Pie or Donut Chart with percentage labels

![Segment](https://github.com/user-attachments/assets/c2478e0a-315f-44eb-b703-af019332bf99)

---

### 🌍 5. Country-wise Sales
**Goal:** Analyze geographic sales distribution.

**Steps:**
- Pivot Table with `Country` and `Sales`
- Use conditional formatting or create a Map Chart
- Highlight top-selling countries

---

### 🥇 6. Top 5 Subcategories
**Goal:** Discover the best-performing subcategories.

**Steps:**
- Pivot Table: `Sub-Category` + `Sales`
- Sort in descending order
- Filter Top 5 only
- Column Chart for visualization

---

### 🚫 7. Bottom 5 Subcategories
**Goal:** Highlight underperforming subcategories.

**Steps:**
- Similar to above but sort in ascending order
- Filter Bottom 5 only
- Use contrasting colors to emphasize performance gap

---

### 📆 8. Yearly Sales Trends
**Goal:** Track performance across years.

**Steps:**
- Group `Order Date` by Year
- Add `Sales` to values
- Line Chart for trend overview
- Use slicers for category/region/segment filtering

---

## ⚙️ Dynamic Features Included
- **Real-time Charts** that respond to slicer selections
- **Power Query Integration** for automated data refresh
- **KPI Table** for quick executive-level metrics

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
- Power Query
- Pivot Tables & Charts
- Conditional Formatting & Slicers

---

## 📎 Project Status
✅ Completed initial version  
🚀 Planned enhancements underway

---

## 📬 Contact
For feedback, suggestions, or collaboration, feel free to reach out via GitHub Issues or contact me directly.

---


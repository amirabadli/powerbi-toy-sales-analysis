## 🎯 Project Title
Analyzing toy sales trends in Mexico to uncover seasonal, regional and product performance patterns.

<img width="632" alt="image" src="https://github.com/user-attachments/assets/c546dcb6-980a-4d1c-ad55-f0e7a52f4088" />

## 📌 **Project Overview**

This Power BI project was developed to enhance my data visualization skills, deepen my understanding of DAX for creating insightful metrics, and strengthen my analytical thinking using the Maven Toys dataset from Maven Analytics.

Focusing on **toy sales data in Mexico (2022–2023)**, the dashboard explores performance across **product categories** and **store locations**.  
The goal is to **identify sales patterns** and **translate them into clear, compelling narratives** to support **business decision-making**.

## 🎯 Key Objectives

- Analyze sales trends over time and across different areas.
- Identify high-performing product categories and their contribution to overall performance.
- Present meaningful insights through interactive visuals.

## 🔧 Data Cleaning & Preparation
Performed basic **data cleaning** and **transformation** steps to support analysis and reporting, including:

- Renamed tables to follow a **star schema structure** such as fact and dimension tables.
- Adjusted data types for some columns to **ensure accuracy** in calculations and visuals.
- **Created calculated columns** to establish a **custom date hierarchy** after marking the ‘Date’ table.
- **Created DAX measures** for four main KPIs: Total Sales, Total Profit, Total Cost, and Profit Margin.
- **Established relationships** between fact and dimension tables to **support accurate filtering** and **aggregation**.

## 📊 Dashboard Overview
- **KPI Cards:** Displays high-level metrics including Total Sales, Total Profit, Total Cost, and Profit Margin.
- **Time Series Charts:** Tracks quarterly performance of sales to highlight seasonal trends.
- **Product Category Breakdown:** Compares sales and profitability across product categories to identify best-performing segments.
- **Top Cities Bar Chart:** Highlights the top 5 cities contributing most to overall revenue.
- **Interactive Slicers:** Filters by year, quarter, and store location, to support deeper analysis.

## 💡 Key Insights
### **Overall performance:**
<img width="593" alt="image" src="https://github.com/user-attachments/assets/103f19bc-3ebe-4d4a-af55-67b0076af057" />
- Across 2022 and 2023, **sales consistently peaked in Q2** ($2.02M (2022) and $2.16M (2023)) and **Q4** ($2.46M in 2022) suggesting **recurring seasonal demand**, possibly tied to school holidays or festive seasons.
<img width="596" alt="image" src="https://github.com/user-attachments/assets/cd7e4a8c-cfe0-453f-a500-48e7cf759f4f" />
- In both 2022 and 2023, **Q3 showed a seasonal drop in total sales** (-19% and -13%, respectively). However, **total costs declined more sharply** (-22% and -13.5%), leading to a **profit margin increase** from 28% to 30.8% in 2022, and 25.7% to 26% in 2023. This may reflect **effective cost control**. The sales decline is likely **correlates to summer holidays in Mexico** (based on Mexico’s holiday timeline), when spending pattern shifts possibly toward non-retail activities.
  
### **Product-level insights**:
<img width="308" alt="image" src="https://github.com/user-attachments/assets/15df1d5b-d03e-4619-a215-9e1b69496656" />
- **Electronics led both profit and profit margin in Q1 2022**, generating approx. $200K in profit. **By Q1 2023, the profit had fallen** by nearly 40% to to around $122K despite stable margins, pushing it from first to third rank in profit. This decline is likely **driven by lower sales**, which also dropped from $410K in Q1 2022 to $303K in the same period previous year.
<img width="307" alt="image" src="https://github.com/user-attachments/assets/e04790de-e117-417a-955d-52d59cb6e3c2" />
- **Art & Crafts and Toys were the top 2 profit generators in 2023** (~$160K and ~$170K respectively), however their **profit margin is consistently low**, with Toys having the lowest margin overall. This performance suggests that these categories **benefited from high volume sales of lower-priced items**.
  
### **Store-level insights**:
<img width="308" alt="image" src="https://github.com/user-attachments/assets/c3d731b9-3d16-4819-b399-8eb8f23a8f74" />
- **Sales fluctuated across all store locations**, with peaks observed in **Q2 and Q4 of 2022**, and **continued to grow in Q1** and **Q2** of 2023. **Downtown consistently led performance**, generating $4.2M in 2022 and $4.0M in 2023.
<img width="309" alt="image" src="https://github.com/user-attachments/assets/87c722ee-f0f1-4bdc-8638-91d56c976987" />
- Notably, **the first half of 2023 saw strong momentum across nearly all locations**, especially **Downtown** and **Commercial**, indicating a **favorable seasonal** or **promotional effect**.
<img width="250" alt="image" src="https://github.com/user-attachments/assets/a19204d8-711e-4a8e-88d7-e3b6a3fecff4" />

- At the city level, **Ciudad de Mexico** consistently emerged as **top contributor in sales** across all years and quarters, reaffirming its role as the company’s key market.
## Recommendations:

- **Product level strategy:**
    - Since Arts & Crafts and Toys were performing well in sales volume but not in profit margin, consider bundle promotions to help increase customer retention and repeat purchases.
    - As for Electronics, which drop from top to third in profit despite stable margin, investigate what contributes to the declining sales such as price changes, shift in customer preference, or competitor offerings.
- **Focus on high profit cities:** Maintain or increase inventory and marketing efforts in Ciudad de Mexico, specifically in downtown and commercial stores to maximize returns.
- **Timing of promotions and seasonality:** Consider planning key marketing campaigns or promotional events around Q2 and Q4 to capitalize on recurring high demand periods.

## ✅ Recommendations
- **Product level strategy:**
    - Since Arts & Crafts and Toys were performing well in sales volume but not in profit margin, consider bundle promotions to help increase customer retention and repeat purchases.
    - As for Electronics, which drop from top to third in profit despite stable margin, investigate what contributes to the declining sales such as price changes, shift in customer preference, or competitor offerings.
- **Focus on high profit cities:** Maintain or increase inventory and marketing efforts in Ciudad de Mexico, specifically in downtown and commercial stores to maximize returns.
- **Timing of promotions and seasonality:** Consider planning key marketing campaigns or promotional events around Q2 and Q4 to capitalize on recurring high demand periods.

## 🧠 DAX Formulas 
```DAX
Total Sales = SUMX(fact_sales, fact_sales[Units] * RELATED(dim_products[Product_Price]))

Total Sales QoQ Diff = 
VAR PrevQuarter =
    CALCULATE ([Total Sales], DATEADD ('dim_calendar'[Date], -1, QUARTER))
RETURN
    IF (ISBLANK (PrevQuarter), 
    BLANK (), 
    [Total Sales] - PrevQuarter)

Total Sales QoQ % Diff =
DIVIDE([Total Sales QoQ Diff], CALCULATE([Total Sales], DATEADD('dim_calendar'[Date], -1, QUARTER)))

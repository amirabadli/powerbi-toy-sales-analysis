*To explore the interactive visuals and slicers, download the [Mexico Toy Sales Performance.pbix](./Mexico%20Toy%20Sales%20Performance.pbix) for complete experience.*

## 🎯 Project Title
Analyzing toy sales trends in Mexico to uncover seasonal, regional and product performance patterns.

<img width="633" alt="image" src="https://github.com/user-attachments/assets/7c867978-f8dd-48b7-aebd-429d4ceb2f10" />


## 📌 **Project Overview**

This Power BI project was developed to enhance my data visualization skills, deepen my understanding of DAX for creating insightful metrics, and strengthen my analytical thinking using the Maven Toys dataset from **[Maven Analytics](https://mavenanalytics.io/)**.

Focusing on **toy sales data in Mexico (2022–2023)**, the dashboard explores performance across **product categories** and **store locations**.  
The goal is to **identify sales patterns** and **translate them into clear, compelling narratives** to support **business decision-making**.

## 🎯 Key Objectives

- Analyze sales trends over time and across different areas.
- Identify high-performing product categories and their contribution to overall performance.
- Present meaningful insights through interactive visuals.

## 🔧 Data Cleaning & Preparation
Performed basic **data cleaning** and **transformation** steps to support analysis and reporting, including:

- Renamed tables to follow a **star schema structure** (e.g: `dim_stores`, `dim_products`, `dim_calendar`, and `fact_sales`).
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
- Across 2022 and 2023, **sales consistently peaked in Q2** ($2.02M in 2022 and $2.46M in 2023). **Q4 2022** also showed a **strong peak** ($2.16M), indicating that the **recurring seasonal demand** likely tied to school holidays or festive seasons and seems that **similar peak** can be **expected in Q4 2023**.
  
<img width="307" alt="image" src="https://github.com/user-attachments/assets/17a154b1-2e66-4e61-8336-280761f4876a" />(2022)
<img width="306" alt="image" src="https://github.com/user-attachments/assets/2cc73132-9508-437e-b483-ec038a18cbb5" />(2023)


- In both 2022 and 2023, **Q3 consistently saw a seasonal drop in total sales**, declining by 19% and 13% respectively from the previous quarter. However, **total cost decreased even more sharply** in 2022 (-22%) and showed a **proportionate decline in 2023** (-13.5%). This effective cost control led to a slight **improvement in profit margin** in both years. The overall sales decline is likely correlates with summer holidays in Mexico (based on Mexico’s holiday timeline), when spending pattern shifts possibly toward non-retail activities during this period. 

<img width="590" alt="image" src="https://github.com/user-attachments/assets/3da301d6-b14e-440c-982e-8ac7a52a4707" /> (Q3 2022)

<img width="590" alt="image" src="https://github.com/user-attachments/assets/cd7e4a8c-cfe0-453f-a500-48e7cf759f4f" /> (Q3 2023)
  
### **Product-level insights**:
- **Electronics led both profit and profit margin in Q1 2022**, generating approx. $200K in profit. **By Q1 2023, the profit had fallen** by nearly 40% to to around $122K despite stable margins, pushing it from **first to third rank in profit**. The decline in Electronic category is likely **driven by lower sales**, which **dropped** from $410K in Q1 2022 to $303K in **Q1 2023**.

<img width="308" alt="image" src="https://github.com/user-attachments/assets/15df1d5b-d03e-4619-a215-9e1b69496656" /> (Q1 2022)
<img width="306" alt="image" src="https://github.com/user-attachments/assets/4ad7be51-61be-484b-8bd9-cd7cafd8b6b1" /> (Q1 2023)

<img width="306" alt="image" src="https://github.com/user-attachments/assets/8ba730d5-7d4d-4407-9576-0498003b9525" /> (2022)
<img width="306" alt="image" src="https://github.com/user-attachments/assets/fec9f997-a08f-4bc3-a9f5-99405e5ef273" /> (2023)


- **Art & Crafts and Toys were the top 2 profit generators in 2023** (~$160K and ~$170K respectively), however their **profit margin is consistently low**, with **Toys** having the **lowest margin overall**. This performance suggests that these categories **benefited from high volume sales of lower-priced items**.

<img width="306" alt="image" src="https://github.com/user-attachments/assets/8995c9c9-edb1-4f53-be40-cf239cca4174" />

  
### **Store-level insights**:
- **Sales fluctuated across all store locations**, with **peaks observed in Q2 and Q4 of 2022**. Following the Q4 surge, sales appeared **strong with QoQ growth** through **Q1 and Q2 of 2023** before eventually **dropping in Q3 2023**.  
- Notably, **the first half of 2023 saw strong momentum across nearly all locations**, especially **Downtown** and **Commercial**, indicating a **favorable seasonal** or positive impact of **promotional efforts**.
  
<img width="308" alt="image" src="https://github.com/user-attachments/assets/c3d731b9-3d16-4819-b399-8eb8f23a8f74" /> (2022)
<img width="306" alt="image" src="https://github.com/user-attachments/assets/d1ff44db-4d68-4c5b-9aaf-8d940d596184" /> (2023)

- At the city level, **Ciudad de Mexico** consistently emerged as **top contributor in sales** across all years and quarters, reaffirming its role as the company’s key market.

<img width="306" alt="image" src="https://github.com/user-attachments/assets/a19204d8-711e-4a8e-88d7-e3b6a3fecff4" />

## ✅ Recommendations
- **Product level strategy:**
    - Since Arts & Crafts and Toys were performing well in sales volume but not in profit margin, consider bundle promotions to help increase customer retention and repeat purchases.
    - As for Electronics, which drop from top to third in profit despite stable margin, investigate what contributes to the declining sales such as price changes, shift in customer preference, or competitor offerings.
- **Focus on high profit cities:** Maintain or increase inventory and marketing efforts in Ciudad de Mexico, specifically in downtown and commercial stores to maximize returns.
- **Timing of promotions and seasonality:** Consider planning key marketing campaigns or promotional events around Q2 and Q4 to capitalize on recurring high demand periods.

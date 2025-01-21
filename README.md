# Housing Sales Analysis

## Overview
This repository contains a comprehensive analysis of housing sales data across various cities, focusing on identifying key trends and patterns in the real estate market. The analysis leverages SQL queries within a Jupyter Notebook environment to explore and summarize the dataset, uncovering actionable insights into sales trends, median prices, and seasonal variations.

---

## Features

### **Exploratory Data Analysis**
- **Key Metrics Extracted**:
  - Total sales by city, year, and month.
  - Mean annual sales trends.
  - Identification of high and low sales periods.
- **Insights Derived**:
  - Cities with consistently high sales activity.
  - Seasonal trends affecting sales volumes.
  - Median price correlations with sales counts.

### **SQL Queries and Use Cases**
1. **Filtering and Aggregation**:
   - Identified records with sales greater than 100 and a median price exceeding $100,000.
   - Analyzed monthly trends for sales surpassing specific thresholds.
2. **Ranking and Grouping**:
   - Highlighted cities and years with the highest mean annual sales, excluding specific city prefixes.
   - Determined which months within specific cities had peak sales activity.
3. **Comparative Analysis**:
   - Compared sales trends across cities while isolating key outliers.
   - Examined attrition trends during peak and off-peak seasons.

### **Advanced Queries**
- Ranked city-month combinations with the highest sales.
- Identified the least active sales periods and locations.
- Highlighted years with significant mean sales increases or decreases.

---

## Key Visualizations
- **Heatmaps**: Correlation between median prices and sales volumes.
- **Tables**: Summary statistics of sales trends by year and city.
- **Line Graphs**: Seasonal sales patterns.

---

## Workflow

1. **Data Preparation**:
   - Integrated SQLite database (`housing.db`) into the Jupyter environment.
   - Cleaned and formatted data for seamless querying.
2. **SQL Query Development**:
   - Constructed queries to analyze specific aspects of the dataset, such as sales counts and price ranges.
3. **Insights Extraction**:
   - Summarized results to highlight trends and anomalies.
   - Generated visualizations to support data interpretation.

---

## Sample SQL Query
```sql
SELECT 
    city, 
    year, 
    AVG(sales) AS mean_annual_sales 
FROM 
    housing 
WHERE 
    city NOT LIKE 'H%' 
GROUP BY 
    city, year 
ORDER BY 
    mean_annual_sales DESC 
LIMIT 20;
```

---

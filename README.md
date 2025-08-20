# Comprehensive_Analysis_of_Fragrances_in_the_E-Commerce_Market
---
# Data Cleaning Steps

This document outlines the steps taken to clean and prepare the men's perfume dataset for analysis.

---

## 🧹 Cleaning Process

1. **Brand Column**
   - Deleted rows with blank cells in the `brand` column.

2. **Type Column**
   - Deleted rows with blank, `/`, or `NA` values in the `type` column.

3. **Price Column**
   - Split the `priceWithCurrency` column into:
     - `currency`
     - `price`
   - Deleted the new `price` column.

4. **Available Column**
   - Filled blank spaces in the `available` column:
     - If `availableText` = "only one remaining" → filled with `1`.
     - If `availableText` = "limited quantity" → marked as `"limited quantity"`.

5. **Sold Column**
   - Replaced blank spaces in the `sold` column with `0`.

6. **Available Text Column**
   - Deleted the `availableText` column after processing.

7. **Last Updated Column**
   - Split the `lastUpdated` column into:
     - `lastUpdatedDate`
     - `lastUpdatedTime`
   - Backfilled blank spaces.
   - Set data types to `Date` and `Time` using Power Query.

8. **Item Location Column**
   - Split `itemLocation` into components.
   - Extracted **country** only.
   - Deleted other split parts.
   - Renamed the country column back to `itemLocation`.

9. **Title Column**
   - Deleted the `title` column (not needed for analysis).

---

## ✅ Result
The cleaned dataset is now consistent, structured, and ready for **Power BI analysis**.


# Perfume Market Report  

## 1. Overview  
- **Revenue:** $102.55 billion  
- **Total Sales:** 1 million units  
- **Average Price:** $43.20 per item  
- **Top Selling Brand:** Versace  

The perfume industry has seen massive growth, especially from 2023 to 2024, where revenue jumped from almost $0 to $102 billion.  

---

## 2. Regional Insights  
- The **United States** dominates sales with about $75K in item price value.  
- Other regions like **Hong Kong ($6K)**, **Canada ($1K)**, and **Taiwan ($1K)** contribute smaller amounts.  
- Many regions show little to no recorded sales.  

---

## 3. Gender Distribution  
- **Men account for more purchases than women.**  
- Male buyers drive a larger share in both sales and revenue.  
- Female buyers still represent an important customer segment.  

---

## 4. Pricing & Availability  
- **Most expensive type:** Eau de Parfum/Perfume ($124.99)  
- **Other premium types:** EDC ($110.19), Eau de Toilette ($92.00), Dior Homme ($89.99)  
- **Popular mid-range types:** Gift Sets ($85.04), Extrait De Parfum ($80.58), Eau De Parfum 2 ($79.59)  

**Price Distribution:**  
- Most perfumes cluster between **$22.50 – $27.49**.  

**Availability vs Sold:**  
- Limited edition perfumes (0.40M units) drive the largest sales.  
- Other categories range from 0.01M to 0.28M sales.  

---

## 5. Customer Preferences  
### Sales by Gender  
- Male buyers: **0.70M units**  
- Female buyers: **0.49M units**  

### Revenue by Gender  
- Revenue is higher for **male buyers** compared to females.  

### Top Brands by Sales  
1. **Versace** – 128K units  
2. **Calvin Klein** – 92K units  
3. **Davidoff** – 60K units  
4. **Burberry & Azzaro** – 38K units each  
5. **Dolce & Gabbana & Liz Claiborne** – 29K units each  

Other brands like Kenneth Cole, Paco Rabanne, Ralph Lauren, Elizabeth Taylor, Vera Wang, and Hugo Boss sold between **20K–25K units**.  

---

## 6. Key Takeaways  
- The perfume market has **exploded in revenue**, led by **Versace and Calvin Klein**.  
- **Men buy more perfumes than women**, contributing to higher sales and revenue.  
- **Premium perfumes** (Eau de Parfum, Eau de Toilette, Dior Homme) command the highest prices.  
- The **U.S. market dominates**, but other regions contribute smaller shares.  

---

## 🔗 Project Link  
[Perfume Market Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzBmY2MwM2MtOGJjYy00NDA5LThhYjEtNzg5MTI4ZWQ5M2Y4IiwidCI6ImQ5ZDBlYmNhLWEyMGYtNDI0My1iMjU4LWVkMTk1M2UwZWQ1OCJ9)  


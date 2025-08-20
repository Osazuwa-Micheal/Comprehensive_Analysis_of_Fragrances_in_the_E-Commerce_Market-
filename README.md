# Comprehensive_Analysis_of_Fragrances_in_the_E-Commerce_Market-
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

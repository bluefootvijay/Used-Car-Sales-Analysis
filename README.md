# Cars24 - Used Car Price & Inventory Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Libraries](https://img.shields.io/badge/Libraries-Pandas%20|%20Seaborn%20|%20Matplotlib-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## Project Overview
In the competitive online used-car marketplace, setting the right price is crucial for profitability and turnover speed. This project analyzes a dataset of over 19,000 used cars to help a dealer optimize pricing strategies and inventory decisions. 

By analyzing factors like car specifications, brand value, and usage history, this project provides a scientific basis for valuation rather than relying on guesswork.

---

## Table of Contents
- [Project Overview](#-project-overview)
- [Business Problems](#-business-problems)
- [Data Dictionary](#-data-dictionary)
- [Analysis Workflow](#-analysis-workflow)
- [Key Insights](#-key-insights)
- [Strategic Recommendations](#-strategic-recommendations)
- [Technologies Used](#-technologies-used)

---

## Business Problems
1.  **Pricing Drivers:** What are the main factors influencing `selling_price`? (e.g., Engine size, Brand, Year).
2.  **Fuel Impact:** Does fuel type (Diesel vs. Petrol) significantly affect resale value when controlling for age?
3.  **Transmission Premium:** How much more do Automatic cars sell for compared to Manual versions of the same model?
4.  **Depreciation Trends:** Quantify the depreciation rate over time—do Luxury cars depreciate faster than Premium cars?
5.  **Mileage Myth:** Do cars with higher fuel efficiency (km/liter) actually command higher resale prices?

---

## Data Dictionary
The analysis is based on the `cars24-car-price.csv` dataset containing **19,980 records**:

* **Target Variable:** `selling_price` (in Lakhs)
* **Car Details:** `full_name`, `year`, `fuel_type`, `transmission_type`, `seats`.
* **Technical Specs:** `engine` (cc), `max_power` (bhp), `mileage` (kmpl).
* **Usage:** `km_driven` (Total kilometers on odometer).
* **Seller Info:** `seller_type` (Dealer, Individual, Trustmark Dealer).

---

## Analysis Workflow

### 1. Data Preprocessing & Feature Engineering
* **Data Cleaning:** Validated dataset for null values and correct data types.
* **Feature Extraction:**
    * Extracted `Make` (Brand) and `Model` from the `full_name` column.
    * Created a **`Segment`** column to categorize cars into **"Luxury"** (e.g., BMW, Audi) and **"Premium"** (e.g., Maruti, Hyundai) for differentiated analysis.
* **Outlier Handling:** Identified outliers in Price, KM Driven, and Engine size using Boxplots.

### 2. Exploratory Data Analysis (EDA)
* **Market Composition:** Analyzed inventory distribution. **Maruti** is the dominant brand (25%), and 80% of stock is Manual transmission.
* **Bivariate Analysis:** Used heatmaps to check correlations. Found that `selling_price` is highly correlated with `max_power` (0.73) and `engine` (0.58), but weakly correlated with `mileage`.
* **Segmentation:** Comparison of "Luxury" vs. "Premium" segments showed distinct depreciation patterns and price drivers.

---

## Key Insights

### 1. What Drives Price? 💰
* **Power is King:** The strongest predictor of price is **Max Power** and **Engine Displacement**. Buyers pay for performance.
* **Mileage Paradox:** Contrary to popular belief, high mileage (fuel efficiency) has a weak *negative* correlation with price. This is because expensive, powerful cars tend to have lower mileage but higher resale value.

### 2. Inventory Dynamics 🚙
* **Dominant Brands:** **Maruti**, **Hyundai**, and **Honda** make up the bulk of the "Premium" inventory, offering high liquidity.
* **Transmission Shift:** While 80% of the inventory is Manual, Automatic cars are commanding higher prices and growing in popularity, especially in the Luxury segment.
* **Seller Type:** 60% of cars are sold by Dealers, indicating a shift away from direct Individual-to-Individual sales.

---

## Strategic Recommendations

Based on the data, the following strategies are recommended for the dealer:

1.  **Pricing Model:**
    * **Action:** Build a pricing algorithm heavily weighted on **Engine Size**, **Max Power**, and **Model Year**. Do not over-weight fuel efficiency (mileage) for valuation.

2.  **Inventory Mix:**
    * **Action:** Maintain a high volume of **Toyota and Honda** models. They show steadier resale values compared to other brands.
    * **Luxury Segment:** Be cautious with high-mileage Luxury cars (BMW, Audi). Their value drops sharply after a certain usage threshold compared to Premium cars.

3.  **Transmission Strategy:**
    * **Action:** Aggressively acquire **Automatic** transmission cars. With only 20% market share but high demand/price, this is a growth opportunity.

4.  **Depreciation-Based Buying:**
    * **Action:** Purchase inventory based on brand-specific depreciation curves. Buy brands with steeper early depreciation (like Luxury) slightly later in their lifecycle (3-5 years old) to maximize margin.

---

## Technologies Used
* **Python:** Core analysis.
* **Pandas:** Data manipulation and Feature Engineering.
* **Seaborn & Matplotlib:** Visualizations (Heatmaps, Boxplots, Bar Charts).

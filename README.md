Used-Car Marketplace Pricing Optimization

This project analyzes a dataset of over 25,000 used-car listings (from 1991 to 2021) to uncover the primary factors that influence resale value. The goal is to provide a data-driven, scientific approach to price setting for a used-car marketplace, empowering dealers with actionable insights for better decision-making.

1. Feature Engineering
   
To improve model accuracy and capture market nuances, several new features were engineered:

Premium/Luxury Segmentation: Cars were classified into market segments (e.g., luxury, premium, standard) based on their brand.

Brand Depreciation Metric: A brand-level metric was created to quantify the average depreciation rate, serving as a proxy for brand-associated value retention.

2. Key Findings & Correlations
   
A correlation analysis was performed to identify which features had the strongest relationship with the selling_price:

Strong Correlation: max_power (0.73) and engine_capacity (0.58) showed a strong positive relationship with price.

Weak Correlation: mileage (km driven) surprisingly showed a weak influence on the final selling price when considered in isolation.

3. Hypothesis Testing
   
To validate observations from the exploratory analysis, hypothesis testing was conducted to confirm the statistical significance of key factors. The results confirmed that fuel type, kilometers driven, and the engineered brand depreciation metric all have a statistically significant effect on the resale price of a vehicle.

Visualizations & Impact

The analysis is supported by a varietyD of clear visualizations created to communicate insights effectively to stakeholders (e.g., dealers, pricing analysts):

Heatmaps (for correlation)

Box Plots (to compare price distributions across categories like fuel type)

Histograms (to understand the distribution of key features like price and mileage)

These insights directly support dealer decision-making by providing a clear understanding of what drives value in the used-car market.

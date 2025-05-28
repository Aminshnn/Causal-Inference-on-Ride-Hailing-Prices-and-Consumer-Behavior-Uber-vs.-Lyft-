# Causal-Inference-on-Ride-Hailing-Prices-and-Consumer-Behavior-Uber-vs.-Lyft-

This project applies causal inference and regression modeling to analyze pricing strategies and rider behavior on Uber and Lyft platforms. It uses real-world trip data to answer two key questions:

&emsp; **1. Does Uber systematically charge more than Lyft under similar trip conditions?**

&emsp; **2. Do customers shift toward upper-tier rides during surge pricing events?**

## Objectives
- Quantify pricing differences between Uber and Lyft under controlled conditions

- Identify interaction effects by ride type, distance, and weather

- Examine consumer decision-making during surge pricing using logistic regression

The data includes features such as trip distance, ride type, platform (cab_type), pickup and drop-off locations, time of day, and weather conditions including temperature and rain. To ensure comparability between platforms, vehicle types were standardized into five common tiers: Shared, Standard, XL, Premium, and Premium XL. Less frequent or non-aligned categories (e.g., Lux, WAV) were excluded.

For pricing analysis, I log-transformed ride prices to correct for skewness and employed Ordinary Least Squares (OLS) regression to estimate percentage differences in price. The baseline model found that Uber charges approximately 5.9% more than Lyft, on average, after controlling for trip characteristics. However, this difference is not uniform. When interaction terms were introduced, the analysis revealed that Uber is actually cheaper in Premium ride tiers but significantly more expensive for Shared rides—up to 40% more.

Additional models explored how price sensitivity varies with distance and rain. Uber’s prices rise more slowly than Lyft’s as distance increases, suggesting more competitive pricing for long trips. Furthermore, during rainy conditions, Lyft tends to lower prices by around 4%, while Uber does not change its pricing—resulting in Uber becoming relatively more expensive in bad weather.

To analyze consumer behavior during surge pricing, I fit a **logistic regression model** predicting whether a rider chose an upper-tier ride (e.g., Premium, XL, or Premium XL). The results show that during surge pricing events, the **odds of selecting a higher-tier ride increase by approximately 2.1 times**. This suggests that surge pricing may not deter customers from costly options—in fact, due to limited availability or reduced price gaps between tiers, users may be nudged into more expensive selections.

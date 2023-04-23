# Commodity_Portfolio_Optimization


## Executive Summary
We partnered with Swiss Re to build personalized portfolios that help individuals hedge against their unique inflation risk. In our current inflationary environment, individuals’ consumption of everyday commodities is becoming increasingly expensive. However, an individual’s inflation exposure is determined by their unique consumption patterns, and as such, no two individuals have the exact same inflation exposure. Thus, we envisioned that no two individuals should have the same inflation-hedging strategy. By predicting future commodity prices using publicly available market and macroeconomic data, our team created an optimized portfolio of commodities that reduces an individual’s inflation exposure by 82%. 

## Dataset
Our team faced ambiguity while designing a solution for this well-researched, but unsolved problem. Economists and academics continue to disagree on what data best models commodity inflation. We conducted extensive research to select data from the infinite options within public market datasets. The team loaded and tested over 30 datasets, and ultimately, historical commodity prices, commodity futures, interest rates, US consumption, US GDP, market volatility, industrial production, money supply, and gold prices showed the most promise. Our final dataset was coalesced into monthly rate changes to accommodate the public macroeconomic datasets available to us. While we were unable to spend more time in data collection, we recommend collecting high-frequency supply, demand, import, and export data that maintains volume, and granularity, and provides leading indications of commodity inflation in future work on this project. 


## Commodity Price Prediction
Initial data analysis revealed that each commodity has different, and somewhat random trends. Therefore each commodity would need to be modeled individually. The team decided to model five aggregated commodity indices (agriculture, energy, industrial metals, precious metals, and livestock) that impact everyday consumers as proof of concept. Our baseline model used only previous prices to predict the price 3 months into the future. Next, we used linear models to regress additional data, and forward/backward selection to identify the best features, which often varied for each commodity. After several iterations of ensemble modeling and time-series forecasting methods, our Fb Prophet time series model was able to predict commodity prices 3 months into the future within 5-10% MAE ($) and outperformed the baseline model by up to 45%. 

## Trading Strategy
Finally, our team built a robust optimization model that used our price forecasts to personalize a portfolio of commodity investments that best hedges against an individual’s unique inflation exposure based on their worst-case consumption and risk appetite. We modeled uncertainty in the user's consumption because it is unreasonable to expect a user to have truly static consumption patterns. Our optimization model successfully created a portfolio that reduced exposure to inflation by 82% (under a full-risk scenario) compared to full exposure with no commodity investments.

Please refer to the report for more details.

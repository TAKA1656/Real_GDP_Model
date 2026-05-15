# Analysis of Macroeconomic Data and Modeling of Real GDP 
Takahiro Hikida
16 May 2026

## Introduction
### Motivation
When the Federal Reserve (US' central bank) raises interest rates or unemployment spikes, the impact on Economic Growth (GDP) doesn't happen overnight. Instead, economic variables act like falling dominoes, where a shock in one area creates a ripple effect that takes months or even years to fully materialize.

While simple correlations can show us what the economy looks like at a specific snapshot in time, they fail to capture these crucial time delays (lags) and chain reactions. I wanted to look beyond the surface and mathematically decode the hidden engine of the economy.

### Questions asked
1. How has the US economy evolved over time?
2. How long does economic variables take to affect the Economic Growth?
3. Does "Consumer Sentiment" (how people feel about the economy) actually drive real Economic Growth, or is it merely statistical noise?
4. To what extent can we mathematically model and predict the structural portion of Economic Growth, separating it from unpredictable external shocks?

### The Approach
To answer the questions above, I had to learn and implement a new technique: the VAR (Vector AutoRegression) model and Impulse Response Function (IRF) analysis.

Unlike simple linear regression, a VAR model consists of a system of equations that allows multiple variables to influence each other over time. By combining this advanced time-series technique with interactive Plotly visualizations, I have built a data narrative that simulates how an initial "shock" (like a sudden rate hike) ripples through the US economy.

### Data Used
I used the data all from Federal Reserve Bank of St.Louis as csv files.
* University of Michigan: Consumer Sentiment (UMCSENT) from Federal Reserve Bank of St.Louis
* Federal Funds Effective Rate (FEDFUNDS) from Federal Reserve Bank of St.Louis
* Consumer Price Index for All Urban Consumers: All Items in U.S. City Average (CPIAUCSL) from Federal Reserve Bank of St.Louis
* Unemployment Rate (UNRATE) from Federal Reserve Bank of St.Louis
* Real Gross Domestic Product (GDPC1) from Federal Reserve Bank of St.Louis

## Procedure  
1. Data Collection and Wrangling

2. Visualizing the Macroeconomic Landscape over Time
Before feeding the data into a complex mathematical model, it is crucial to visually inspect the historical trends of our variables. The time-series plots above illustrate the dynamic behavior of the U.S. economy over the past few decades.

Key Observations:

* Major Economic Shocks: We can clearly identify massive spikes and drops in the Economic Growth Rate and Unemployment Rate, particularly around the 2008 Financial Crisis and the 2020 COVID-19 pandemic. These are profound, unpredictable external shocks.

* Inverse Relationships: Visually, there appears to be a natural friction between the Unemployment Rate and Economic Growth—when one spikes, the other plummets.

* The "Lag" Intuition: If you look closely at the Federal Funds Rate and Inflation, their peaks and valleys do not always perfectly align with the dips in Economic Growth. They seem to trail behind or precede the growth curve, confirming our initial hypothesis: economic variables do not react instantly; they operate on a time delay.   

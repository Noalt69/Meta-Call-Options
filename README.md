# Hedging Call Options on Meta Stock

## Background
This project focuses on hedging call options using Meta’s stock as the underlying asset. The primary goal was to explore financial risk management strategies through Delta hedging and Delta-Vega hedging. Hedging is a crucial financial practice aimed at reducing risk exposure due to unpredictable market price movements, commonly used by finance professionals dealing with derivatives.

The analysis was performed using options data imported from Refinitiv Workspace, specifically focusing on Meta call options with a strike price of 585 and a time to maturity of 45 days.

## Hedging Methods
### Delta Hedging:
- **Objective:** Minimize directional risk by neutralizing portfolio exposure to the underlying asset's price movements.
- **Method:** Continuous rebalancing by adjusting the quantity of the underlying asset held.
- **Performance:** More frequent rebalancing (daily) showed lower mean squared error (MSE), indicating better performance compared to less frequent (weekly) hedging. However, increased rebalancing also led to higher transaction costs.

### Delta-Vega Hedging:
- **Objective:** Mitigate both price risk and volatility risk using a combination of the underlying asset and a secondary replicating option with longer maturity.
- **Method:** Delta hedging is supplemented with Vega adjustments using a second call option for additional volatility control.
- **Performance:** Outperformed Delta hedging during periods of significant volatility changes. However, frequent rebalancing was again more effective but costly.

### Portfolio Hedging:
- A portfolio of call options was also hedged using both strategies. Challenges were noted, especially when managing multiple options due to volatility and transaction costs.

## Conclusion
- **Hedging Frequency:** More frequent rebalancing improved performance but increased transaction costs.
- **Delta vs. Delta-Vega Hedging:** Delta-Vega hedging proved superior in volatile conditions but still faced challenges when applied to portfolios.
- **Recommendations:** Incorporate higher-order Greeks and account for transaction costs in future hedging strategies for improved real-world applicability.

This report is part of the Financial Risk Management with Derivatives course (TU-E2211), Aalto University, Autumn 2024.

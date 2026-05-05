# Risk & Exposure Analytics Accelerator

Enterprise-grade portfolio risk analytics with credit modeling, market VaR, operational risk monitoring, stress testing, and ML-powered default predictions — built as a Snowflake Native App.

## Features

### Executive Summary
- Composite Risk Heat Score combining credit, market, operational, and capital factors
- Natural language risk intelligence search
- Capital Adequacy Ratio trend with Basel III threshold
- Geographic exposure by US state

### Credit Risk
- Expected Loss calculation (PD x LGD x EAD)
- NPA ratio monitoring and loan status breakdown
- Sector-level exposure and loss analysis
- PD distribution and credit rating exposure

### Market Risk
- Value at Risk (VaR) at 95% and 99% confidence levels
- Portfolio volatility and asset class breakdown
- VaR contribution analysis by asset type
- Position value tracking over time

### Operational Risk
- Loss by event type and severity classification
- Monthly loss trends and event frequency
- Business line loss attribution
- Critical event monitoring

### Stress Testing
- Interactive scenario parameters (IR shock, PD multiplier, LGD adjustment)
- Baseline vs stressed expected loss comparison
- Sector-level stress impact analysis
- Sensitivity curves (EL vs PD multiplier)

### ML Default Predictions
- Logistic regression model trained on portfolio data
- Real-time loan risk classification (Low/Medium/High)
- Loss driver analysis with factor importance
- Recovery strategy recommendations

## Required Data Tables

After installing, bind these 5 table references:

| Reference | Key Columns |
|-----------|-------------|
| Customers | CUSTOMER_ID, NAME, SEGMENT, COUNTRY, RISK_RATING |
| Loans | LOAN_ID, CUSTOMER_ID, LOAN_AMOUNT, INTEREST_RATE, TENURE, PD, LGD, EAD, STATUS, SECTOR |
| Market Positions | POSITION_ID, ASSET_TYPE, MARKET_VALUE, VOLATILITY, DELTA, POSITION_DATE |
| Operational Events | EVENT_ID, EVENT_TYPE, LOSS_AMOUNT, DATE, SEVERITY, BUSINESS_LINE |
| Capital Metrics | METRIC_DATE, TIER1_CAPITAL, TIER2_CAPITAL, RISK_WEIGHTED_ASSETS, TOTAL_CAPITAL, CAR |

## Permissions

The app requests SELECT access on bound tables. All analytics run in-place on your Snowflake warehouse. No data leaves your account.

## Version History

| Version | Date | Notes |
|---------|------|-------|
| 1.0.0 | 2026-05-05 | Initial marketplace release |

Tesla DCF Valuation (Python)
Overview
This project presents a full 10-year Discounted Cash Flow (DCF) valuation of the automotive company of Tesla, Inc. (TSLA), built completely from scratch in Python. The objective of this project was to estimate Tesla’s intrinsic value based on the projected free cash flows and then compare it to the current market price. 

Conclusion: 
Under conservative, data driven assumptions, Tesla’s main automotive business appears highly overvalued. The data driven model implies an intrinsic value of approx. $16.56 per share (core automotive business based), compared to the current market price of roughly $360, suggesting that most of Tesla’s valuation is based on the expectations of Tesla’s future ventures, currently non-cashflow generating business (ex: FSD, robotaxies, and optimus robots). 


Tools & Data
Python (Pandas, NumPy, Matplotlib)
Jupyter Notebook
Data: Macrotrends, Tesla Investor Relations (10-K / filings)


Methodology
1. Revenue Forecasting
Historical growth (2020–2025) shows clear deceleration from rapid growth to contraction. Instead of extrapolating averages, a two-stage forward model was constructed:
2026–2027: Continued decline (pricing pressure, competition, demand normalized)
2028: Stabilization
2029–2032: Moderate recovery
2033–2035: Mature growth (3–5%)
This approach prioritizes recent trend relevance over distorted historical averages.

2. Margin Assumptions
Operating margins declined from 16.8% (2022) to 4.6% (2025), primarily due to pricing pressure and elevated R&D.
Near-term compression followed by gradual recovery
Terminal margin capped at 9.5%, well below peak levels
This reflects structural competition and capital intensity, not a full reversion to peak profitability.




3. Capital Intensity (D&A and Capex)
D&A modeled with decelerating growth (13% → 9%)
Capex anchored to recent 3-year average, grown at 4%
This avoids unrealistic assumptions of either:
Hyper-expansion, or
Sudden capital efficiency


4. Free Cash Flow Construction
FCF calculated as:
FCF = Operating Income + D&A – Capex
Key insight: Tesla’s automotive segment generates minimal near-term free cash flow due to heavy reinvestment.
2026 FCF: ~$0.37B
2035 FCF: ~$15.9B

5. Cost of Capital (WACC)
WACC reflects Tesla’s risk profile:
Risk-Free Rate: 4.3%
Beta: 1.93
Market Risk Premium: 5.5%
Cost of Equity: 14.92%
After-tax Cost of Debt: 3.95%
Capital Structure: ~99.5% equity
WACC: 14.86%
The elevated discount rate is driven almost entirely by equity risk and volatility.

6. Valuation
PV of FCFs: $25.5B
PV of Terminal Value: $33.0B
Enterprise Value: $58.4B
Implied Share Price: $16.56
Terminal growth rate: 2.5%, aligned with long-term nominal GDP.

7. Sensitivity Analysis
A 3×3 sensitivity grid (WACC vs. terminal growth) shows:
Even optimistic scenarios → max value ≈ $26/share
Implies persistent and significant valuation gap

Key Insight
A change in assumptions could not possibly account for the size of the valuation gap.
This implies that Tesla’s current valuation is largely based on future option value rather than today’s car sales. 
Specifically:
Full Self Driving (FSD)
Robotaxi network
Humanoid robotics (Optimus)
Energy storage expansion
The market is pricing in high-probability success of multiple (future) business lines.


Limitations
No working capital adjustments
No segment-level modeling (energy, services)
No explicit modeling of speculative revenue streams (by design)
This model intentionally isolates the value of currently observable, cash-flow-generating operations.

Takeaway
My analysis does not claim Tesla is “wrongly priced,” but rather clarifies what must be true for the current valuation to be justified.
At ~$360/share, investors are not buying Tesla’s present (automotive core) business — they are underwriting a set of high-uncertainty, high-upside future outcomes.

Notes for Reviewers
All assumptions are explicitly modeled and can be adjusted. The goal of this project is not to be 100 percent accurate, but to be able to make a valuation based on transparent and defensible claims based on my understanding of valuation logic. 

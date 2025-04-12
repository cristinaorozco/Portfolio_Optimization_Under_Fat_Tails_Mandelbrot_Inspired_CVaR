#  Portfolio Optimization under Fat Tails – Inspired by Mandelbrot

This project presents a portfolio optimization model based on fractal market theory, particularly inspired by the ideas of Benoît Mandelbrot, who challenged traditional assumptions of Gaussian behavior in financial markets. Unlike classical Markowitz models, this approach accounts for fat tails and extreme events by simulating returns using a Student's t-distribution and optimizing the portfolio based on Conditional Value at Risk (CVaR).

---

# Objective

To build a robust asset allocation model that maximizes the expected return adjusted by the risk of extreme losses. Instead of relying on mean-variance optimization, we use CVaR (95%) as the core risk metric to represent potential loss in the worst scenarios.

---

# Methodology

1. Asset Selection
   - High-volatility, high-tech stocks: `AAPL`, `TSLA`, `NVDA`, `AMD`, `META`, `AMZN`.
   - Historical data from Yahoo Finance (2020–2024).

2. Return Modeling  
   - Daily log-returns are calculated.
   - Fat-tailed distributions are modeled using Student’s t-distribution (df = 3).

3. Portfolio Simulation
   - 10,000 portfolios with random weights (fully invested)
   - For each portfolio:
     - Expected return is calculated.
     - CVaR (95%) is computed using Monte Carlo simulation of 1,000 returns from the t-distribution.
     - An adjusted performance ratio is calculated. 
  
4. Optimization Output 
   - Optimal portfolio = highest Adjusted Ratio.
   - Visualization of all portfolios in CVaR vs Return space, with the optimal point highlighted.

---

# Python libraries Used

- yfinance
- numpy
- pandas
- matplotlib
- scipy.stats.t (Student’s t-distribution)

---

# Results

- A portfolio that outperforms classical mean-variance allocations under non-Gaussian assumptions.
- Clear evidence of the impact of fat tails on risk metrics.
- A visual frontier where the optimal balance between return and tail-risk is highlighted.
- Optimal portfolio weights.

---

# Key Insights

- Gaussian assumptions underestimate risk in real markets.
- CVaR is more robust than standard deviation in capturing downside risk.
- This approach better reflects real-world behavior and market crises.


---

# Author

Cristina Orozco.  
Quantitative Researcher | Risk Model Developer | Data Scientist  
Focused on building robust, data-driven solutions for financial decision-making.

LinkedIn: www.linkedin.com/in/cristina-orozco


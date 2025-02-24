# finance
Repository where I show code in Python related to finances

## Crypto Portfolio Optimization.
[Link to Repo](https://github.com/juanesc396/finance/blob/main/crypto_portfolio_optimization.ipynb)

Portfolio optimization aims to construct an asset allocation that maximizes returns while minimizing risk. One key challenge is accurately estimating the covariance matrix, which quantifies the relationships between asset returns.

A robust approach to improving covariance estimation is Ledoit-Wolf shrinkage, implemented in:

```python
from pypfopt.risk_models import CovarianceShrinkage
cov_matrix = CovarianceShrinkage(returns_df).ledoit_wolf()
```

### Why Ledoit-Wolf Shrinkage?
- Reduces estimation errors by shrinking noisy covariance estimates toward a structured target.
- Improves portfolio stability, especially when dealing with limited historical data.
- Enhances risk-adjusted returns by preventing overfitting in mean-variance optimization.
- This technique is particularly useful in Markowitz's Mean-Variance Optimization (MVO), where an accurate covariance matrix is crucial for determining the Efficient Frontier—the set of optimal portfolios that offer the highest return for a given risk level.

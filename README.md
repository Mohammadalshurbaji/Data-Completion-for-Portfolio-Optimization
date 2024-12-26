## Data Completion in Financial Time Series for Portfolio Optimization

This project investigates the application of data completion techniques for portfolio management and risk modeling. The focus is on using low-rank matrix completion to address missing values in financial time series data.

**Project Motivation:**

Driven by a passion for finance and the stock market, this project explores portfolio management and risk modeling using low-rank matrix completion with nuclear norm minimization.

**Data and Methodology:**

1. **Data Acquisition:**
   - Employs the `yfinance` library to download stock price data for leading technology companies (AMZN, TSLA, NFLX, NVDA, MSFT, AAPL, CRM) from December 1, 2019, to December 1, 2022.
   - The data is stored in a CSV file named "LeadingTech_stock_prices.csv".

2. **Data Preprocessing:**
   - Calculates daily stock returns using percentage change.
   - Introduces simulated missing data by randomly masking 10% of the values.
   - Normalizes the data for further analysis.

3. **Matrix Completion Techniques:**
   - **Method 1: Singular Value Decomposition (SVD):**
     - Fills missing entries using the mean.
     - Performs SVD on the partially filled matrix to capture its low-rank structure.
     - Reconstructs the completed matrix using a reduced set of singular values.

   - **Method 2: CVXPY Library for Nuclear Norm Minimization:**
     - Formulates a convex optimization problem using CVXPY to minimize the nuclear norm, promoting a low-rank solution.
     - The resulting solution represents the completed data matrix.

4. **Covariance Matrix and Portfolio Optimization:**
   - Calculates the covariance matrix for both completion methods to assess risk relationships between assets.
   - Portfolio optimization techniques can be employed on the completed data for portfolio construction.

5. **Evaluation:**
   - The project intends to evaluate the effectiveness of the data completion methods using metrics like:
     - Mean Squared Error (MSE)
     - Mean Absolute Error (MAE)
     - Root Mean Squared Error (RMSE)
     - Frobenius Norm
   - Visualization of the original and completed data's singular values is also planned.

**Overall, this project investigates the potential of data completion techniques to improve the accuracy and robustness of portfolio management and risk modeling in the presence of missing financial data.**

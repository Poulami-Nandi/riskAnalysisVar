# Quantitative Risk Analysis with Value at Risk (VaR)

## Overview

This project provides a **Quantitative Risk Analysis** of a portfolio using **Value at Risk (VaR)** methodology. The analysis calculates VaR using three different methods:

1. **Historical Simulation**
2. **Parametric VaR (using Normal Distribution)**
3. **Monte Carlo Simulation**

The project implements an **Object-Oriented Programming (OOP)** approach, making the code modular, reusable, and scalable.

In addition to VaR, the project extends the analysis by calculating **Conditional Value at Risk (CVaR)** and **Expected Shortfall (ES)**, which are used to assess the tail risks in a portfolio.

### Project Structure

The project is organized into the following sections:
- **Portfolio Class**: Manages assets and computes portfolio returns.
- **RiskModel Class**: Implements the VaR calculation using various methods.
- **AdvancedRiskModel Class**: Extends `RiskModel` to include CVaR and ES.

### **Technologies Used**

- **Python 3.x**
- **pandas** for data handling
- **numpy** for numerical calculations
- **matplotlib** for visualization
- **scipy** for statistical functions
- **yfinance** for downloading financial data
- **scikit-learn** for machine learning and statistical modeling

---

## Features

### 1. **Portfolio Class**
The `Portfolio` class is responsible for fetching stock data and calculating portfolio returns.

- **Methods**:
    - `fetch_data`: Downloads stock data for a list of tickers.
    - `portfolio_returns`: Calculates portfolio returns based on asset weights.

### 2. **RiskModel Class**
The `RiskModel` class calculates the **Value at Risk (VaR)** of the portfolio using multiple methods.

- **Methods**:
    - `historical_var`: Calculates VaR using the historical simulation method.
    - `parametric_var`: Calculates VaR using the parametric (normal distribution) method.
    - `monte_carlo_var`: Calculates VaR using Monte Carlo simulations.
    - `visualize_var`: Visualizes VaR results and portfolio return distribution.

### 3. **AdvancedRiskModel Class**
The `AdvancedRiskModel` class extends `RiskModel` and calculates additional risk metrics such as **Conditional Value at Risk (CVaR)** and **Expected Shortfall (ES)**.

- **Methods**:
    - `conditional_var`: Calculates CVaR (average loss beyond VaR).
    - `expected_shortfall`: Calculates the expected shortfall (tail risk) of the portfolio.

### 4. **Data Visualization**
The project includes various visualizations that compare different VaR methods and assess portfolio risk:

- Histogram of portfolio returns
- VaR calculations visualized using vertical lines
- CVaR and ES visualized on the return distribution

---

## Installation

To install the necessary dependencies, simply clone the repository and install the packages using **pip**.

### Clone the repository

```bash
git clone https://github.com/Poulami-Nandi/riskAnalysisVar.git
Install required packages
pip install -r requirements.txt
```
---
## Project Folder Structure

riskAnalysisVar/
│
├── data/
│   └── historical_data.csv      # Store downloaded data 
│
├── src/
│   └── riskAnalysisVar.py        # Python file for VaR calculation
│
├── results/
│   └── vaR_results.csv          # Store the results of the different VaR methods
│
├── notebooks/
│   └── riskAnalysisVar.ipynb  # Jupyter notebook with explanation and analysis
│
└── README.md                    # Project description and instructions
└── requirements.txt             # requirements.txt file


---
## Usage
- Clone the repository.
- Download financial data using Yahoo Finance (the stock tickers in the portfolio can be customized).
- Run the analysis by invoking the RiskModel or AdvancedRiskModel class to calculate VaR, CVaR, and ES.

```bash
python riskAnalysisVar.py
```

### Example of Output
After running the analysis, the following output is generated:
```bash
Historical VaR (95% confidence): -2.50%
Parametric VaR (95% confidence): -2.45%
Monte Carlo VaR (95% confidence): -2.52%
```
Additionally, visualizations are provided in the form of histograms comparing portfolio returns and VaR.

## Visualizations
- **1. Portfolio Returns Distribution**
The histogram shows the distribution of portfolio returns over the specified time period.

- **2. VaR Comparison**
The Value at Risk is visualized using vertical lines to indicate the levels of risk calculated using different methods.

- **3. Conditional VaR and Expected Shortfall**
The Conditional VaR (CVaR) and Expected Shortfall (ES) are plotted to understand the tail risks of the portfolio.

---

## Advanced Features
- Stress Testing and Scenario Analysis
Future improvements can include implementing stress testing and scenario analysis to evaluate how the portfolio would behave under extreme market conditions (e.g., 2008 financial crisis).

- Portfolio Optimization
Additional work could involve optimizing the portfolio to minimize risk and maximize return by adjusting the asset weights based on the calculated VaR, CVaR, and ES metrics.

---

## License
This project is licensed under the MIT License - see the LICENSE file for details.

---
##References
Value at Risk (VaR) Methods: Wikipedia
Monte Carlo Simulation: Wikipedia
Yahoo Finance API: yfinance GitHub
Contributing

Feel free to open an issue or create a pull request if you have any suggestions or improvements to the project!

Example of Visual Output:
Value at Risk Calculation:

A bar plot visualizing the time taken by each method to compute VaR.
A histogram comparing portfolio returns, with VaR, CVaR, and ES shown as lines.
Stress Testing:

A scenario plot visualizing portfolio performance under extreme market conditions.

---
## Final Thoughts
This project serves as an introduction to Quantitative Risk Analysis and demonstrates practical applications of Value at Risk (VaR) in financial risk management. With Python, pandas, matplotlib, and scipy, we can effectively analyze and visualize the potential risks in financial portfolios.

GitHub Repository:
[Link to GitHub Repository](https://github.com/Poulami-Nandi/riskAnalysisVar)

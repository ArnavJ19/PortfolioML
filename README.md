# 🚀 Quantifying Market Dynamics: A Data-Driven Portfolio Allocation & Performance Analysis 📊

## Introduction

Financial markets are dynamic ecosystems where macroeconomic shifts, volatility, and sector rotations influence asset performance. Traditional portfolio allocation methods, such as sector-based diversification, often fail to capture the true risk-return relationships between assets.

This project explores a **clustering-driven portfolio construction** methodology, benchmarking its performance against the **S&P 500** and the **Magnificent 7** over the period **2021–2025**. By leveraging **Hierarchical Clustering** to group stocks based on return-volatility profiles, the strategy seeks to optimize diversification and enhance risk-adjusted returns.

---

## 🔬 Methodology

### 1️⃣ Data Collection & Preprocessing
- Historical stock prices from **2021–2025** were obtained from [Yahoo Finance](https://finance.yahoo.com/) and other market data sources.
- Data cleaning, missing value imputation, and outlier handling were performed to ensure accuracy.
- **Returns and volatility** were computed for each stock to define its risk-return characteristics.

### 2️⃣ Hierarchical Clustering for Asset Segmentation
- Unlike traditional sector-based allocation, we employed **Hierarchical Clustering** to segment stocks based on their return-volatility profiles.
- The clustering process involved:
  - **Distance Metric**: Euclidean Distance applied to normalized return-volatility vectors.
  - **Linkage Method**: Ward’s method to minimize intra-cluster variance.
  - **Cluster Selection**: Optimal number of clusters determined using **Dendrogram Analysis**.
- Stocks within each cluster exhibited **similar risk-return characteristics**, ensuring logical diversification.

### 3️⃣ Momentum-Based Stock Selection
- From each identified cluster, the **top 10 stocks** with the highest cumulative returns over a rolling window were selected.
- This selection ensured momentum-driven exposure across diversified clusters.

### 4️⃣ Portfolio Construction
- The final portfolio was constructed using **equal-weight allocation**, distributing capital evenly across the selected high-momentum stocks.
- **Equal weighting** was chosen to prevent excessive concentration risk in any single asset.

### 5️⃣ Backtesting & Performance Analysis
- The strategy was **rigorously backtested** across different market regimes, including the 2022 bear market.
- Performance was benchmarked against:
  - **S&P 500 Index** – Representative of broad market performance.
  - **Magnificent 7** – A high-growth technology-heavy portfolio.
- Key evaluation metrics included **annualized return, volatility, drawdowns, and risk-adjusted return (Sharpe Ratio).**

---

## 📈 Performance Insights

### 📊 Overall Performance (2021-2025)

| Metric           | Portfolio  | S&P 500  | Magnificent 7 |
|-----------------|-----------|---------|--------------|
| **Annual Return** | 35.36%    | 13.87%  | 35.55%       |
| **Volatility**   | 19.11%    | 16.49%  | 30.23%       |
| **Sharpe Ratio** | 1.75      | 0.72    | 1.10         |
| **Sortino Ratio** | 2.56     | 1.01    | 1.62         |
| **Treynor Ratio** | 0.32     | 0.12    | 0.21         |
| **Calmar Ratio** | 2.06      | 0.55    | 0.72         |
| **Max Drawdown** | -17.19%   | -25.42% | -49.39%      |

### 📊 2022 Performance (Bear Market)

| Metric           | Portfolio  | S&P 500  | Magnificent 7 |
|-----------------|-----------|---------|--------------|
| **Annual Return** | 13.67%    | -17.13% | -40.53%      |
| **Volatility**   | 26.59%    | 24.17%  | 42.38%       |
| **Sharpe Ratio** | 0.44      | -0.79   | -1.00        |
| **Sortino Ratio** | 0.69     | -1.26   | -1.65        |
| **Treynor Ratio** | 0.11     | -0.19   | -0.26        |
| **Calmar Ratio** | 0.79      | -0.67   | -0.82        |
| **Max Drawdown** | -17.19%   | -25.42% | -49.13%      |


### ✅ Long-Term Performance
- **Portfolio Annual Return**: **35.36%**  
- **S&P 500 Annual Return**: **13.87%**  
- **Magnificent 7 Annual Return**: **35.55%**  
- The portfolio **outperformed the S&P 500 significantly**, demonstrating the effectiveness of the strategy.
- Despite slightly trailing the Magnificent 7, the portfolio exhibited **lower volatility and drawdowns**, making it a **more stable** investment.

### ✅ Risk-Adjusted Strength
- **Sharpe Ratio** (Higher is better):  
  - **Portfolio**: **1.75**  
  - **S&P 500**: **0.71**  
  - **Magnificent 7**: **1.80**  
- The Sharpe Ratio confirms **strong risk-adjusted performance**, ensuring **higher returns per unit of risk taken.**

### ✅ Outperformance in the 2022 Bear Market
- **2022 Returns Comparison:**
  - **Portfolio**: **+13.67%** ✅  
  - **S&P 500**: **-17.13%** ❌  
  - **Magnificent 7**: **-40.53%** ❌  
- While major indices suffered **significant drawdowns**, the portfolio **remained profitable**, demonstrating strong downside protection.

---

## 💡 Key Takeaways

### 🔹 Clustering-Based Stock Selection Enhances Diversification
- Traditional sector-based allocation does not always reflect true risk-return characteristics.
- **Hierarchical Clustering** ensures assets are grouped based on **actual performance similarities**, improving diversification.

### 🔹 Momentum-Driven Selection Works
- Selecting the **top-performing** stocks within each cluster **enhanced returns** while maintaining diversification.
- This **avoids overexposure** to single themes and adapts dynamically to market trends.

### 🔹 Equal-Weighting Provides Stability
- Many portfolios overweight large-cap stocks, leading to **concentration risk**.
- **Equal-weight allocation** distributes risk more evenly and reduces over-reliance on a few high-performing stocks.

---

## 🔍 Next Steps

### 🔹 Paper Publication & GitHub Release
- The **findings** from this project will be published in a **scientific paper**, detailing the methodology, results, and implications.
- The **full methodology & code** will be released on **GitHub** after further refinements.

### 🔹 Future Enhancements
- Incorporating **additional risk factors** such as macroeconomic indicators and sector rotations.
- Exploring **adaptive weighting mechanisms** that adjust based on market conditions.
- Enhancing **machine learning-driven selection** for **dynamic portfolio optimization**.

---
### Overall Results 
![Overall_RV](https://github.com/user-attachments/assets/7b26bf01-4930-4e72-88c8-1e9e11c15232)
![Overall_PV_Returns](https://github.com/user-attachments/assets/7f6a0712-d9df-47e4-8d93-7995cb95b5bb)
![Overall_Drawdown](https://github.com/user-attachments/assets/23f7d334-9f79-4f8c-a15f-d8423c3c258c)
![Overall_CR_Returns](https://github.com/user-attachments/assets/1ddb8223-c5ca-4020-a876-90417e136e38)

### Perfomance during the 2022
![PV_2022](https://github.com/user-attachments/assets/3e68e17c-4d22-4eac-a2f6-8da9a5ffd254)
![CR_2022](https://github.com/user-attachments/assets/e55b72c9-7f2f-4c18-8f54-df491081183c)
![Drawdown_2022](https://github.com/user-attachments/assets/36de1f23-751c-4bdd-b7d2-48ed5d10ec15)
![Distribution_2022](https://github.com/user-attachments/assets/157f570d-58fc-4a97-93f2-794e2131cd95)
![RV_2022](https://github.com/user-attachments/assets/18253404-30fb-4a51-adca-b6ecfe6968ad)

### Portfolio Allocations
![Allocation](https://github.com/user-attachments/assets/59099db9-7421-44b8-aeb0-3a08a7b00e95)





## 🚀 Getting Started

### 1️⃣ Installation & Setup
Clone the repository and install required dependencies:

```bash
git clone https://github.com/yourgithubusername/market-dynamics-portfolio.git
cd market-dynamics-portfolio
pip install -r requirements.txt

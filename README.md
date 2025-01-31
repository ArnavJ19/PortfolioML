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

## 🚀 Getting Started

### 1️⃣ Installation & Setup
Clone the repository and install required dependencies:

```bash
git clone https://github.com/yourgithubusername/market-dynamics-portfolio.git
cd market-dynamics-portfolio
pip install -r requirements.txt

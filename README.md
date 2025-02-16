
# Stock Analysis with Python

This repository contains a Python script for analyzing historical stock data, including detecting price trends, identifying best days to short-sell, tracking after-hours trading, using Bollinger Bands for market forecasting, and analyzing stock movements on high trading volume days.

## Features

The stock analysis script performs the following tasks:

1. **Finding Best Stocks to Short-Sell (Largest Price Drops)**
   - Identifies the worst 10 days based on the largest price drops using percentage change.
   
2. **After-Hours Trading Impact**
   - Analyzes the largest after-hours price changes by comparing the opening price of the next day with the closing price of the previous day.
   
3. **Using Bollinger Bands for Market Forecasting**
   - Calculates the Bollinger Bands (upper and lower) and compares them with the closing prices to analyze market conditions.
   
4. **Identifying Periods of Steady Increase and Decline**
   - Analyzes stock price trends (increasing or decreasing) based on daily changes and counts periods of steady increase or decline.
   
5. **Optimal Buy Day for Holding Until Now**
   - Identifies the optimal day to buy (the day with the lowest closing price).
   
6. **Stock Movement on High Trading Volume Days**
   - Identifies stock movements (up or down) on days with high trading volume (above the 90th percentile of the volume).

## Requirements

To run this analysis, you'll need the following Python packages:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

You can install the required dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn
```

## Files

1. **`stock_analysis.py`** - Contains the main script for the stock analysis.
2. **`HistoricalQuotes.csv`** - The CSV file containing historical stock data. (You need to replace this path with the location of your own stock data file.)

## Usage

1. **Load the CSV file**:
   Ensure that the CSV file (`HistoricalQuotes.csv`) contains columns such as `Date`, `Open`, `High`, `Low`, `Close/Last`, and `Volume`. Make sure the `Date` column is in the proper datetime format.

2. **Run the Analysis**:
   Run the script using a Python environment (e.g., Jupyter notebook or directly in the terminal):

```bash
python stock_analysis.py
```

3. **Output**:
   The script will print out the following results:
   
   - Worst 10 days for short-selling (stocks with the largest price drops).
   - Top 10 after-hours price changes.
   - Bollinger Bands chart comparing stock price with upper and lower bands.
   - Trend analysis (Increase or Decrease).
   - Optimal buy day for holding until now.
   - Stock movement on high trading volume days (Up or Down).

## Example Output

**Worst 10 Days for Short-Selling:**
```plaintext
          Date    Close/Last  Daily_Change
5   2025-02-15  132.10        -0.15
...
```

**Top 10 After-Hours Changes:**
```plaintext
          Date    Open    Close/Last  After_Hours_Change
2   2025-01-05   130.50  132.60        2.10
...
```

**Bollinger Bands Chart:**
A chart will be displayed showing the closing prices along with the upper and lower Bollinger Bands.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

This analysis uses Python libraries `pandas`, `numpy`, `matplotlib`, and `seaborn` for data manipulation, analysis, and visualization.


# Algorithmic Trading Market Data Repository

A curated collection of high-resolution market data, optimized for quantitative analysis and algorithmic trading strategy backtesting.

***

## 📊 Data Description

This repository contains historical market data. The data is provided in `.csv` format for easy use with common data analysis libraries like pandas.

The data is organized according to the following hierarchy:

* **`asset_class`**: The type of financial asset.
    * *Examples: `stocks`, `crypto`*

* **`data_type`**: The nature of the data stored in the CSV file.
    * *Examples: `ohlc` (Open, High, Low, Close), `ticks`*

* **`currency`**: The currency in which the asset is denominated.
    * *Examples: `usd`, `eur`, `jpy`*

* **`period`**: The time frequency of the data points.
    * *Examples: `1min`, `5min`, `1s`, `daily`*

* **`symbol`**: The filename, which is the ticker symbol of the instrument.
    * *Examples: `AAPL`, `BTC`*

### OHLC (Open, High, Low, Close)

Each row in the dataset includes the following columns:

* **`timestamp`**: The start time interval (e.g., in UTC).
* **`open`**: The price at the beginning of the interval.
* **`high`**: The highest price reached during the interval.
* **`low`**: The lowest price reached during the interval.
* **`close`**: The price at the end of the interval.
* **`volume`**: The total trading volume during the interval.
* **`price`**: The volume-weighted average price (VWAP) for the interval, calculated as `Σ(Price * Volume) / Σ(Volume)`.

***

## 🚀 Getting Started

To get started, you can clone this repository or download the specific dataset you need.

Here is a quick example of how to load and inspect the data using **Python** and the **pandas** library:

```python
import pandas as pd

# Load a dataset
# Make sure to replace 'path/to/your/datafile.csv' with the correct file path
df = pd.read_csv("path/to/your/datafile.csv", parse_dates=["timestamp"], index_col="timestamp", sep=";")

# Print the first 5 rows of the dataframe
print("Data Head:")
print(df.head())

# Get a quick statistical summary of the data
print("\nData Description:")
print(df.describe())
```

## ⚠️ Disclaimer

This data is provided for educational and research purposes only. It is not intended as financial advice. We do not guarantee the accuracy, completeness, or timeliness of the data. Trading financial instruments involves risk, and you should use this data at your own discretion.

## Sponsorship

If you find this project helpful and would like to support its continued development, please consider becoming a sponsor. Your sponsorship helps me dedicate more time to maintaining this repository and adding new features. Thank you for your support!

[Sponsor this project](https://github.com/sponsors/blaizard)

## 🤝 Contributing

Contributions are welcome! If you find any issues, have suggestions for new datasets, or want to improve the existing data, please feel free to open an issue or submit a pull request.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

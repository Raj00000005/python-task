# Python Tasks – Hangman Game & Stock Forecast App

This repository contains two Python projects developed as part of a Python programming task:

1. **Hangman Game** – a graphical word-guessing game built with Tkinter.
2. **Stock Forecast App** – an interactive Streamlit application that downloads historical stock data and generates future price forecasts using Facebook Prophet.

---

## 📁 Repository Structure

```text
python-task/
│
├── README.md
├── hangman_game.py
└── stock_tracker.py
```

---

# 🎮 1. Hangman Game

## Description

The Hangman Game is a desktop GUI application developed using **Python and Tkinter**. The player attempts to guess a hidden word by entering letters. The application provides visual feedback for correct and incorrect guesses and displays the game result when the word is completed or the player runs out of chances.

## Features

- Graphical user interface using Tkinter
- Random word selection
- Letter-by-letter guessing
- Correct and incorrect guess handling
- Displays the current word progress
- Tracks remaining chances
- Win and loss notifications
- Option to play again
- Simple and user-friendly interface

## Technologies Used

- Python
- Tkinter
- Random module

## How to Run

Make sure Python is installed on your computer.

```bash
python hangman_game.py
```

Tkinter is normally included with standard Python installations.

---

# 📈 2. Stock Forecast App

## Description

The Stock Forecast App is an interactive web application built with **Streamlit**. It retrieves historical stock-market data using **Yahoo Finance**, displays historical opening and closing prices with Plotly, and generates future forecasts using **Prophet**.

## Supported Stocks

The application provides the following stock choices:

- GOOGL – Alphabet
- AAPL – Apple
- MSFT – Microsoft
- GE – General Electric

## Features

- Interactive stock selection
- Historical stock-data download
- Historical opening and closing price visualization
- Prediction-period selection from **1 to 4 years**
- Future date generation
- Prophet-based forecasting
- Interactive Plotly charts
- Forecast data displayed in the Streamlit interface
- Forecast components can be visualized for analysis

## Technologies Used

- Python
- Streamlit
- yfinance
- Prophet / Facebook Prophet
- Plotly
- Pandas

## Installation

Install the required packages:

```bash
pip install streamlit yfinance plotly
```

The source code currently imports Prophet using:

```python
from fbprophet import Prophet
```

If your environment uses the newer Prophet package, install:

```bash
pip install prophet
```

and update the import in `stock_tracker.py` to:

```python
from prophet import Prophet
```

## How to Run

Open a terminal in the project folder and run:

```bash
streamlit run stock_tracker.py
```

Streamlit will start a local web server and provide a browser link to open the application.

---

# 🔄 Stock Forecast Workflow

```text
Select Stock
     ↓
Download Historical Data
     ↓
Display Raw Data
     ↓
Plot Opening & Closing Prices
     ↓
Prepare Date + Closing Price Data
     ↓
Train Prophet Model
     ↓
Generate Future Dates
     ↓
Predict Future Prices
     ↓
Display Forecast & Forecast Components
```

---

# 📊 Stock Forecast Methodology

The application uses historical **closing prices** as the target variable.

The data is prepared in the format required by Prophet:

| Column | Description |
|---|---|
| `ds` | Date |
| `y` | Closing stock price |

The Prophet model is then trained using the historical data and used to generate predictions for the selected number of future years.

---

# 🛠️ Requirements

Recommended environment:

- Python 3.x
- pip
- Internet connection for downloading stock data
- Modern web browser for the Streamlit application

For the Stock Forecast App, the main dependencies are:

```text
streamlit
yfinance
plotly
prophet / fbprophet
```

---

# ⚠️ Important Notes

- The Stock Forecast App requires an internet connection because it downloads market data from Yahoo Finance.
- Stock forecasts are statistical predictions and **should not be considered financial advice**.
- Forecast accuracy depends on the quality and historical behavior of the selected stock.
- The Hangman Game runs locally and does not require an internet connection.

---

# 🚀 Future Improvements

Possible enhancements include:

- Add more stocks and indices
- Add technical indicators such as SMA, EMA and RSI
- Add candlestick charts
- Add forecast confidence intervals
- Add downloadable forecast reports
- Improve Hangman graphics
- Add difficulty levels to the Hangman Game
- Add a larger word database
- Add score tracking and leaderboard functionality

---

# 👨‍💻 Project

**Python Programming Task**

This repository demonstrates Python programming concepts including:

- GUI development
- Functions and control flow
- Randomization
- Data collection through APIs
- Data processing
- Data visualization
- Time-series forecasting
- Interactive web application development


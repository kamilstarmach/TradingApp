# 📈 Stock News Alert (Tesla Example)

This project monitors the daily price movement of a stock (in this example: **TSLA – Tesla Inc**).  
If the price changes by more than 1%, it fetches the latest news articles related to the company  
and sends them to your phone via **Twilio SMS**.

---

## 🔧 Features

- Fetches daily stock price data from **Alpha Vantage API**
- Calculates the percentage difference between the two most recent trading days
- If the movement exceeds 1%, retrieves breaking news from **NewsAPI**
- Formats the top 3 articles with headline + short description
- Sends each article as a separate SMS using **Twilio**

---

## 📦 Requirements

- Python 3.8+
- Accounts + API keys for:
  - **Alpha Vantage**
  - **NewsAPI**
  - **Twilio** (SID, Auth Token, verified phone number)

---

## 🔌 Installation

1. Clone the repository:

```bash
git clone https://github.com/your-repo/stock-news-alert.git
cd stock-news-alert
Install dependencies:


pip install requests twilio
🔑 Configuration
Open the Python script and replace placeholders with your actual credentials:

python

VIRTUAL_TWILIO_NUMBER = "+123456789"
VERIFIED_NUMBER = "+48123456789"

STOCK_API_KEY = "YOUR_ALPHA_VANTAGE_API_KEY"
NEWS_API_KEY = "YOUR_NEWSAPI_KEY"
TWILIO_SID = "YOUR_TWILIO_SID"
TWILIO_AUTH_TOKEN = "YOUR_TWILIO_AUTH_TOKEN"
Important:
Do NOT commit real API keys to GitHub. Use environment variables or a .env file.

▶️ How to Run

python main.py
If the price difference exceeds 1%, you will receive 3 SMS messages similar to:


TSLA: 🔺3%
Headline: Tesla opens new Gigafactory.
Brief: The company aims to increase production...
🧠 How It Works
Fetch daily time series from Alpha Vantage

Extract closing prices from the two most recent days

Calculate the absolute and percentage changes

Fetch related news articles if the threshold is exceeded

Format each article into SMS-ready text

Send messages through Twilio's REST API

⚠️ Security Notes
Use environment variables (.env) with python-dotenv

Never expose your API keys in public repositories

Twilio trial accounts can only send SMS to verified numbers

🚀 Possible Improvements
Support multiple stock tickers (AAPL, NVDA, AMZN, etc.)

Add scheduling using cron or GitHub Actions

Send alerts via Telegram or email instead of SMS

Create a web dashboard for alert configuration

📜 License
MIT License — feel free to use, modify, and expand.











ChatGPT może popełniać błędy. Sprawdź ważne informacje. Zobacz 

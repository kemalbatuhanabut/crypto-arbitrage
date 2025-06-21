# 📈 Crypto Arbitrage Monitor

Real-time **arbitrage opportunity detector** comparing cryptocurrency prices between **Binance** and **Coinbase**.
Built with **pure HTML, CSS, and JavaScript**, it demonstrates **real-time WebSocket streaming** combined with **REST API fetching**, dynamic DOM rendering, and percentage-based arbitrage calculations.

---

## 🚀 Live Demo

*crypto-arbitrage.abut.tr*

---

## ⚙️ Features

✅ **Real-Time Binance Prices** via WebSocket
✅ **Coinbase Prices** via REST API (updates every 3 seconds)
✅ **Multiple Trading Pairs** tracked simultaneously
✅ **Automatic Arbitrage Calculation** (% based)
✅ **Visual Indicators** for arbitrage opportunities
✅ **No Frameworks Required** — runs entirely in the browser

---

## 📂 Technologies Used

| Technology           | Why It's Used                            |
| -------------------- | ---------------------------------------- |
| **HTML5**            | Page structure & semantic markup         |
| **CSS3**             | Clean, responsive visual design          |
| **JavaScript (ES6)** | Core logic & dynamic DOM manipulation    |
| **WebSocket API**    | Real-time, low-latency data from Binance |
| **Fetch API**        | Asynchronous REST calls to Coinbase      |
| **Binance API**      | Real-time ticker prices for crypto pairs |
| **Coinbase API**     | Spot prices fetched for comparisons      |

---

## 🏗️ How It Works

### 📡 1. Real-Time Binance Streaming

* Connects to Binance **WebSocket API** for each selected pair (e.g., `wss://stream.binance.com:9443/stream?streams=btcusdt@ticker`).
* Updates Binance price instantly on every tick.

### 🔄 2. Coinbase Spot Prices

* Queries **Coinbase REST API** (`https://api.exchange.coinbase.com/products/BTC-USD/ticker`) every **3 seconds**.
* Coinbase doesn’t provide free real-time WebSockets, hence the REST polling approach.

### 📊 3. Arbitrage Calculation

For each pair:

```
Arbitrage % = ((BinancePrice - CoinbasePrice) / CoinbasePrice) * 100
```

* Positive % → **Buy Coinbase → Sell Binance**
* Negative % → **Buy Binance → Sell Coinbase**
* > ±0.1% is considered significant and highlighted.

---

## 📦 Example Pairs Supported

* BTC/USDT
* ETH/USDT
* SOL/USDT
* ADA/USDT

*Add or remove pairs easily by modifying the `pairs` array in the script.*

---

## 🖥️ Screenshot Preview

*Add screenshot here if available*

---

## 🛠️ Setup & Run Locally

```bash
git clone https://github.com/kemalbatuhanabut/crypto-arbitrage.git
cd crypto-arbitrage
# Simply open index.html in your browser
```

✅ **No Node.js or dependencies required.**

---

## ⚡ Potential Enhancements

* 📲 **WebSocket Support for Coinbase** *(requires API key or premium account)*
* 📢 **Notifications or Sound Alerts** on arbitrage
* 💰 **Fee/Commission Simulation** for realistic profit calculation
* 📈 **UI Improvements with Tailwind or Bootstrap**
* 📊 **Add Chart Support** for historical price trends

---

## 🏷️ Why This Project?

This project is a **showcase of frontend engineering with live data APIs**.
It demonstrates:

* Real-time data handling
* REST vs WebSocket workflows
* Dynamic HTML generation
* Clean modern CSS practices

If you're into crypto, finance, or trading bots — this is your **foundation project** to build upon.

---

## 🤝 Contributing

Pull requests welcome! Open issues for suggestions, feature requests, or bugs.

---

## 📜 License

MIT License © 2025 \Kemal Batuhan ABUT

---

### ✨ Made with focus on **real-time finance** and **modern web development**.


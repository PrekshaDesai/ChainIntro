# ChainIntro – Web3 & Blockchain Educational Website

ChainIntro is an educational website that helps beginners understand the fundamentals of Web3, Blockchain, and Cryptocurrency through simple explanations and interactive demonstrations. The project combines learning resources with practical examples, making blockchain concepts easier to understand.

# Features

* Responsive landing page
* Web3 and Blockchain concept comparison page
* Live cryptocurrency price dashboard using the CoinGecko API
* Interactive blockchain mining simulator
* SHA-256 hashing demonstration
* Proof-of-Work simulation
* Responsive design for desktop and mobile devices
* Modern and clean user interface

# Project Structure

ChainIntro/
│
├── index.html              # Home Page
├── concepts.html           # Concepts Page
├── prices.html             # Live Prices Page
├── simulator.html          # Blockchain Simulator
│
├── css/
│   └── style.css
│
└── js/
    ├── nav.js
    ├── prices.js
    └── simulator.js
```

# Technologies Used

* HTML5
* CSS3
* JavaScript (ES6)
* Web Crypto API
* CoinGecko API
* Google Fonts

# Website Pages

## 1. Home

* Introduction to Web3 and Blockchain
* Hero section
* Feature section
* Navigation bar
* Footer

## 2. Concepts

This page explains important blockchain concepts using comparison cards.

Topics covered:

* Web2 vs Web3
* Bitcoin vs Ethereum
* Public Key vs Private Key
* Blockchain vs Traditional Database

## 3. Live Prices

This page displays live cryptocurrency prices.

Features:

* Bitcoin (BTC) Price
* Ethereum (ETH) Price
* Current USD Price
* 24-Hour Price Change
* Refresh Button
* CoinGecko API Integration

## 4. Blockchain Simulator

This page demonstrates how blockchain works.

Features:

* Enter block data
* Generate SHA-256 hash
* Mine block using Proof of Work
* Nonce calculation
* Block validation
* Blockchain integrity demonstration
  
# How to Run

1. Clone the repository.
git clone https://github.com/PrekshaDesai/ChainIntro.git

2. Open the project folder.

3. Open **index.html** in your web browser.
Alternatively, you can use the VS Code Live Server extension.

An internet connection is required to load Google Fonts and fetch live cryptocurrency prices.

# How It Works

### Navigation

* A shared navigation bar is available on every page.
* The current page is automatically highlighted using JavaScript.

### Live Cryptocurrency Prices

* Retrieves real-time Bitcoin and Ethereum prices from the CoinGecko API.
* Displays the current price and 24-hour price change.
* Includes a refresh button to update the data.

### Blockchain Simulator

* Uses the browser's Web Crypto API to generate SHA-256 hashes.
* Simulates Proof-of-Work mining by calculating a valid hash.
* Demonstrates blockchain immutability by showing how changing one block affects the next block.

# Learning Objectives

This project helps users understand:

* Web3
* Blockchain
* Cryptocurrency
* Bitcoin
* Ethereum
* SHA-256 Hashing
* Nonce
* Proof of Work
* Blockchain Immutability
* Public and Private Keys

# Future Improvements

* Add support for more cryptocurrencies
* Add cryptocurrency search
* Display price charts
* Dark mode
* Wallet integration
* Enhanced mining animations
* More blockchain learning modules

# Author

Name: Preksha Desai 

GitHub: https://github.com/PrekshaDesai

Batch: 2024-2028

# License

This project was developed for educational purposes as part of a Web3 learning assignment.

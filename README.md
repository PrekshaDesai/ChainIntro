# ChainIntro - Web3 & Blockchain Educational Website

ChainIntro is a premium, production-quality static educational portal designed to introduce beginners to the fundamental concepts of Web3, live cryptocurrency markets, and block mechanics. 

Built using pure **HTML5**, **CSS3**, and **vanilla ES6+ JavaScript**, this project requires **no installation, no npm packages, and no compiler**. It can be executed instantly by opening the `index.html` file in any modern web browser.

---

## 📂 File Structure

```
/web3-edu-site
  ├── index.html          (Page 1: Landing page detailing Web3 pillars)
  ├── concepts.html       (Page 2: Educational side-by-side explainers)
  ├── prices.html         (Page 3: Live CoinGecko ticker dashboard)
  ├── simulator.html      (Page 4: Interactive block hashing workspace)
  ├── /css
  │     └── style.css     (Shared stylesheet: colors, typography, glassmorphism, responsive grid, animations)
  └── /js
        ├── nav.js        (Shared: window.location.pathname active highlighting & scroll observer)
        ├── prices.js     (Page 3 logic: async/await CoinGecko fetches, search validation)
        └── simulator.js  (Page 4 logic: Web Crypto API SHA-256 calculator, PoW mine, chain-breaking)
```

---

## 🚀 Setup and How to Run

1. **Clone or Download** this directory to your local filesystem.
2. Navigate to the project root folder.
3. Locate `index.html` and double-click the file to open it in your default web browser (such as Google Chrome, Firefox, Safari, or Microsoft Edge).
4. *(Optional)* For the best experience, you can serve the directory using a simple static file server (e.g. `npx serve .` or VS Code Live Server extension), although opening the raw path (`file:///`) is fully supported.
5. Make sure you are connected to the internet to load external Google Fonts ("Space Grotesk" & "Inter") and fetch market rates from the CoinGecko API on Page 3.

---

## 🧠 Behind the Scenes: How It Works

This project is tailored for learners. Below are key technical mechanisms explained in detail:

### 1. Active Navigation Highlighting (`nav.js`)
To highlight the current page in the navbar without duplicating code or using server-side rendering, `nav.js` checks the browser's current address:
* On page load, it queries `window.location.pathname` to fetch the path to the current file.
* It extracts the active page name by stripping parent directories (finding the substring after the last `/`).
* It compares this filename (e.g., `concepts.html`) with the `href` attribute of each navigation link.
* When a match is found, it injects the `.active` class into the link, prompting the CSS to render the colorful, glowing underline indicator.

### 2. Client-Side Input Validation
All forms across the site implement basic client-side validation before running calculations or network calls to ensure zero silent errors:
* **Live Prices Search**: Prevents submission if the coin search field is empty or contains non-alphanumeric characters (such as spaces or symbols), which would crash the CoinGecko fetch call.
* **Block Simulator**: Validates that block data is non-empty and that the nonce is a valid, positive integer. If validation fails, input borders flash red and a visible inline error message appears.

### 3. Cryptographic SHA-256 Hashing (`simulator.js`)
Instead of using a mock hash or relying on a large external library, Page 4 employs the **native Web Crypto API** built into modern web browsers:
* The async function `crypto.subtle.digest('SHA-256', msgBuffer)` calculates the true SHA-256 hash.
* `TextEncoder` translates plain text characters into a binary stream before hashing.
* The output binary buffer is then converted into a human-readable 64-character hexadecimal signature.

### 4. The Chain-Breaking Effect (Blockchain Immutability)
The simulator illustrates why blockchain data is tamper-proof:
* Block 2's `Previous Hash` field is dynamically bound to Block 1's computed current Hash.
* When Block 1's data is edited, its hash changes instantly (referred to as the *avalanche effect*).
* Since Block 1's hash updates, the input values to Block 2's hash formula automatically change.
* As a result, Block 2's computed hash updates and fails to meet the required difficulty criteria (starts with `00`), triggering the status badge to switch to **"❌ Block Invalid"** and highlighting the card in red.
* To restore the blockchain, the user is forced to re-mine Block 1, followed by re-mining Block 2.

---

## ✏️ Placeholders to Fill

In the footer of all four HTML files, locate the developer credits block:
* Replace `[YOUR NAME]` with your full name.
* Replace `[YOUR GITHUB URL]` with the web address of your GitHub profile.
* Replace `[YOUR BATCH NAME]` with your course or batch identifier.

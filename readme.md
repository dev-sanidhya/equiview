# Equiview

Equiview is an AI-powered stock analysis CLI tool that simulates the perspectives of multiple types of financial agents to generate a comprehensive view on a given stock ticker. It includes:

- _HedgeFundGPT_: A conservative, metrics-driven analyst.
- _RetailGPT_: A meme-loving, hype-fueled retail investor.
- _NewsBot_: A news-focused agent that analyzes headlines to extract sentiment and catalysts.
- _Debate Engine_: Synthesizes all agent perspectives into a final recommendation.
- _Follow-Up Engine_: Lets users ask follow-up questions and get expert-level answers based on the previous analysis.

---

## 🚀 Features

- Pulls real-time market data from Finhub
- Scrapes latest news headlines using Google News RSS
- Uses Groq-hosted LLMs (via groq runner) for personalized agent prompts
- Compares and debates perspectives to arrive at a final decision
- Allows investors to ask follow-up questions after the main analysis
- CLI-friendly with emoji-enhanced, color-coded outputs using colorama

---

## 🛠 Installation

1. Clone the repo:

bash
git clone https://github.com/dev-sanidhya/equiview
cd equiview

2. Install dependencies:

bash
pip install -r requirements.txt

3. Set up your API keys:

bash
export GROQ_API_KEY="your-groq-key" # For Groq LLM
export FINHUB_API_KEY="your-finhub-key" # For financial data

Or use a .env file to store them.

---

## 💡 Usage

Run the CLI and input a stock ticker:

bash
python main.py

Then follow the prompt to enter a ticker (e.g., AAPL, TSLA, NVDA).

After the agents analyze the stock and deliver their recommendations, you'll also get an option to ask a follow-up question for deeper insight.

---

## 📦 Project Structure

equiview/
├── agents.py # Prompt templates for HedgeFundGPT, RetailGPT, NewsBot
├── debate.py # Merges all agents into a final consensus
├── fetch_data.py # Pulls stock data from Finhub
├── news_fetcher.py # Scrapes headlines from Google News RSS
├── llm_runner.py # Handles LLM API interaction via Groq
├── main.py # CLI runner and controller logic
├── followup.py # Handles follow-up question generation
├── validation.py # Post-processing and validation utilities
└── requirements.txt # Python dependencies

---

## 🔁 Follow-Up Questions

Once the initial analysis is complete, users can ask questions like:

"Why did the NewsBot say SELL for TSLA?"
"Would RetailGPT still buy if interest rates rose?"
"What are the top 3 concerns HedgeFundGPT has?"

These questions are answered using the Groq LLM with reference to the previously generated consensus, allowing for deep, interactive insights.

---

## 🔐 API Keys

- _Groq_: Required for LLM-based prompts.
- _Finhub_: Required for fetching financial data.
- (Optional) Google News RSS (used without authentication)

---

## 🧠 Example Output

🔍 Analyzing Tesla, Inc. (TSLA)
📈 Market Cap: $817.3B | 📁 P/E Ratio: 125.18

✅ HedgeFundGPT: HOLD
✅ RetailGPT: BUY
✅ NewsBot: SELL

🤝 Final Consensus: HOLD
🔥 Risk Level: 4/5
💼 Rationale: Conflicting views require caution.

📣 Investor: "Why did NewsBot recommend SELL?"
🤖 Analyst: Based on recent headlines, NewsBot identified negative sentiment tied to regulatory risk and slowing delivery growth. This informed the SELL recommendation.

---

## 📈 Future Ideas

- Add SocialMediaGPT (Reddit/X sentiment scraping)
- Export results as PDF or Markdown
- Web dashboard for visualizing agent opinions
- Scheduled email digests for watchlist tickers

---

## 📬 Contact

Built by Atharva & Sanidhya. For feedback, collaboration, or feature ideas, feel free to reach out!

---

## 📄 License

MIT License. Use freely with attribution.

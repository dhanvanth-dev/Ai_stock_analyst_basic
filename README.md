# Stock Analyst Agent

A Streamlit app for technical and fundamental stock analysis powered by AutoGen agents and OpenAI-compatible LLMs. Enter a ticker symbol, fetch real market data, compute key indicators, and get a disciplined BUY/HOLD/SELL recommendation with confidence and reasoning.

## Features

- **Real-time Data:** Fetches 1-year daily price history, fast info, and basic financials using [yfinance](https://github.com/ranaroussi/yfinance).
- **Technical Indicators:** Computes SMA20/50/200, RSI, MACD, 52-week high/low, and volume trends.
- **Fundamental Signals:** Extracts market cap, PE ratio, PB ratio, dividend yield, and more.
- **LLM Agent:** Uses AutoGen and OpenAI-compatible models (via OpenRouter) to analyze both technical and fundamental signals and output a strict JSON recommendation.
- **Interactive UI:** Built with Streamlit for easy input, visualization, and agent interaction.

## Setup

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/financial_analysis.git
    cd financial_analysis
    ```

2. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    Required packages include: `streamlit`, `yfinance`, `python-dotenv`, `ta`, `autogen_agentchat`, `autogen_ext`, `openai`, `numpy`, `pandas`.

3. **Set your OpenAI API key:**
    - Create a `.env` file in the project root:
        ```
        OPENAI_API_KEY=your_openai_or_openrouter_api_key
        ```
    - Or set it in your environment:
        ```bash
        export OPENAI_API_KEY=your_openai_or_openrouter_api_key
        ```

4. **Run the app:**
    ```bash
    streamlit run stock.py
    ```

## Usage

- Enter a stock ticker (e.g., `AAPL`, `MSFT`, `TSLA`) in the input box.
- Select the price lookback period (`1y`, `6mo`, `3mo`).
- Click **Analyze**.
- View computed technical and fundamental metrics, price chart, and the agent's recommendation with confidence score and reasoning.

## Notes

- Data is fetched via Yahoo Finance and may be delayed or incomplete for some tickers.
- The agent's output is for educational purposes only and not financial advice.
- The app uses OpenRouter's DeepSeek model by default, but you can configure other OpenAI-compatible endpoints.

## File Structure

- `stock.py` — Main Streamlit app.
- `requirements.txt` — Python dependencies.
- `.env` — Environment variables (API keys).

## License

MIT License

---

*Data via yfinance. This is educational, not

# Trade Sales - AI Trading Simulation Platform

A sophisticated AI-powered trading simulation platform that runs multiple autonomous trading agents with different strategies, models, and personalities. **This is NOT a real trading platform and should not be used for actual trading.**

## 📊 Project Flow Diagrams

For detailed system architecture and trading cycle diagrams, see **[PROJECT_FLOW.md](PROJECT_FLOW.md)** which contains:
- 🔄 **Trading Cycle** - Step-by-step trading process
- 📊 **Simplified Overview** - High-level system flow

## 🎯 Key Features

### **Multi-Agent Trading System**
- **4 AI Traders** with distinct personalities and strategies:
  - **Warren (Patience) [GPT-4o-mini]**: Long-term value investing
  - **George (Bold) [DeepSeek Chat]**: Aggressive growth strategy
  - **Ray (Systematic) [Gemini 2.5 Flash]**: Algorithmic/systematic approach
  - **Cathie (Crypto) [Grok 3 Mini]**: Innovation and crypto-focused

### **Real-time Market Data**
- **Polygon.io Integration** for live market data
- Fallback to random prices when API unavailable
- Support for different Polygon plans (free, paid, realtime)

### **Research Capabilities**
- **Brave Search API** for financial news
- **Web Fetch** for detailed research
- **Persistent Memory** for each trader to build knowledge over time

### **Real-time Dashboard**
- **Gradio Web Interface** with:
  - Live portfolio value tracking
  - Interactive charts
  - Transaction history
  - Real-time logs
  - Holdings overview

## 🚀 Getting Started

### Prerequisites
- Python 3.12+
- UV package manager
- API keys for:
  - Polygon.io (market data)
  - OpenAI/DeepSeek/Gemini/Grok (LLM providers)
  - Brave Search (research)

### Installation
```bash
# Clone the repository
git clone <repository-url>
cd trade_sales

# Install dependencies
uv sync

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys

# Run the trading floor
uv run trading_floor.py

# In another terminal, run the web interface
uv run app.py
```

### Configuration
- `RUN_EVERY_N_MINUTES`: Trading cycle frequency (default: 60)
- `RUN_EVEN_WHEN_MARKET_IS_CLOSED`: Enable 24/7 trading (default: false)
- `USE_MANY_MODELS`: Use different models per trader (default: false)

This platform demonstrates advanced AI agent orchestration for automated trading with multiple strategies, real-time data integration, and comprehensive monitoring capabilities.

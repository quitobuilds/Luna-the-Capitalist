# 🌙 Luna Capitalist

**An autonomous AI agent that identifies and executes money-making opportunities across multiple domains.**

[![Twitter](https://img.shields.io/badge/Twitter-@LunaCapitalist-1DA1F2?style=flat&logo=twitter)](https://x.com/LunaCapitalist)

---

## 🎯 What is Luna Capitalist?

Luna Capitalist is an LLM-powered autonomous agent designed to generate revenue through various online opportunities. It combines market analysis, arbitrage detection, trend prediction, and automated execution across multiple verticals.

## 📊 Revenue Modules

| Module | Description | Risk Level | Automation |
|--------|-------------|------------|------------|
| 🃏 **Trading Cards** | TCG arbitrage, PSA grading predictions, market timing | Medium | Full |
| 📦 **Dropshipping** | Product research, supplier sourcing, trend detection | Low-Medium | Full |
| 📈 **Day Trading** | Technical analysis, momentum plays, risk management | High | Semi |
| 🎨 **NFT Flipping** | Rarity analysis, whale tracking, mint sniping | High | Full |
| 💰 **Crypto Arbitrage** | Cross-exchange spreads, DEX/CEX opportunities | Medium | Full |
| 🏠 **Domain Flipping** | Expiring domains, trend keywords, valuation | Low | Full |
| ✍️ **Freelance Automation** | Gig matching, proposal generation, delivery | Low | Semi |
| 🎮 **Game Item Trading** | In-game economies, skin arbitrage, account services | Medium | Full |
| 📱 **App Store Optimization** | Keyword gaps, clone opportunities, ASO services | Low | Semi |
| 🔄 **Retail Arbitrage** | Price tracking, deal alerts, resale automation | Low | Full |
| 📝 **Content Monetization** | SEO content, affiliate marketing, ad optimization | Low | Full |
| 🎁 **Rewards Farming** | Credit card churning, cashback stacking, points arbitrage | Low | Full |

---

## 🏗️ Architecture

```
luna-capitalist/
├── main.py                 # Main orchestrator
├── config/
│   └── settings.yaml       # Configuration & API keys
├── modules/
│   ├── trading_cards.py    # TCG market analysis
│   ├── dropshipping.py     # E-commerce automation
│   ├── day_trading.py      # Stock/crypto trading
│   ├── nft_flipper.py      # NFT market operations
│   ├── crypto_arbitrage.py # Cross-exchange arbitrage
│   ├── domain_flipper.py   # Domain investment
│   ├── freelance.py        # Gig economy automation
│   ├── game_trading.py     # Virtual item markets
│   ├── aso_services.py     # App store optimization
│   ├── retail_arbitrage.py # Physical goods arbitrage
│   ├── content_monetize.py # Content & affiliate
│   └── rewards_farming.py  # Points & cashback
├── utils/
│   ├── llm_client.py       # LLM API wrapper
│   ├── market_data.py      # Data fetching utilities
│   ├── risk_manager.py     # Position sizing & limits
│   └── notifier.py         # Alerts & notifications
├── data/                   # Local data storage
└── logs/                   # Execution logs
```

---

## 🚀 Quick Start

### Prerequisites

```bash
python >= 3.10
pip install -r requirements.txt
```

### Installation

```bash
git clone https://github.com/yourusername/luna-capitalist.git
cd luna-capitalist
pip install -r requirements.txt
cp config/settings.example.yaml config/settings.yaml
# Edit settings.yaml with your API keys
```

### Run

```bash
# Run all modules
python main.py

# Run specific module
python main.py --module trading_cards

# Dry run (no real trades)
python main.py --dry-run

# Set risk level
python main.py --risk conservative
```

---

## 🔧 Configuration

Edit `config/settings.yaml`:

```yaml
# LLM Settings
llm:
  provider: anthropic  # or openai, local
  model: claude-sonnet-4-20250514
  api_key: ${ANTHROPIC_API_KEY}

# Risk Management
risk:
  max_daily_loss: 100  # USD
  max_position_size: 500
  risk_level: moderate  # conservative, moderate, aggressive

# Module Settings
modules:
  trading_cards:
    enabled: true
    platforms: [tcgplayer, ebay, cardmarket]
    
  dropshipping:
    enabled: true
    platforms: [shopify, amazon]
    
  # ... more modules
```

---

## 📈 Module Deep Dives

### 🃏 Trading Cards Module

Analyzes TCG markets (Pokemon, MTG, Yu-Gi-Oh, Sports Cards) for:
- **Price Arbitrage**: Cross-platform price discrepancies
- **Grading Plays**: Raw cards worth grading (PSA/BGS ROI calculator)
- **Meta Predictions**: Upcoming format changes affecting card values
- **Sealed Product**: Box EV calculations and investment timing

### 📦 Dropshipping Module

Automated e-commerce operations:
- **Product Research**: TikTok/Instagram trend detection
- **Supplier Matching**: AliExpress/1688 price comparison
- **Listing Generation**: AI-powered product descriptions
- **Competitor Tracking**: Price monitoring and adjustment

### 📈 Day Trading Module

Technical analysis and execution:
- **Pattern Recognition**: Chart patterns, support/resistance
- **Sentiment Analysis**: News and social media parsing
- **Risk Management**: Stop-loss, position sizing
- **Backtesting**: Strategy validation before live trading

### 💰 Crypto Arbitrage Module

Cross-exchange opportunities:
- **CEX Spreads**: Binance vs Coinbase vs Kraken
- **DEX/CEX Gap**: Uniswap vs centralized prices
- **Triangular Arb**: Multi-hop currency conversion
- **Funding Rate Arb**: Perpetual vs spot spreads

---

## ⚠️ Risk Disclaimers

1. **Financial Risk**: Trading involves substantial risk of loss
2. **No Guarantees**: Past performance doesn't guarantee future results
3. **Legal Compliance**: Ensure activities comply with local laws
4. **API Terms**: Respect platform ToS and rate limits
5. **Not Financial Advice**: This is experimental software

---

## 🛠️ Development

### Adding New Modules

1. Create module in `modules/your_module.py`
2. Implement the `BaseModule` interface
3. Add configuration in `settings.yaml`
4. Register in `main.py`

```python
from modules.base import BaseModule

class YourModule(BaseModule):
    def analyze(self) -> list[Opportunity]:
        """Find opportunities"""
        pass
    
    def execute(self, opportunity: Opportunity) -> Result:
        """Execute on opportunity"""
        pass
    
    def calculate_risk(self, opportunity: Opportunity) -> float:
        """Return risk score 0-1"""
        pass
```

---

## 📊 Performance Tracking

Luna tracks all operations in `data/performance.db`:
- Win/loss ratio per module
- ROI by strategy
- Risk-adjusted returns
- Execution latency

Dashboard: `python -m utils.dashboard`

---

## 🤝 Contributing

1. Fork the repo
2. Create feature branch
3. Add tests
4. Submit PR

---

## 📜 License

MIT License - Use at your own risk.

---

## 🌙 Follow Luna

- Twitter: [@LunaCapitalist](https://x.com/LunaCapitalist)
- Updates on opportunities found
- Performance transparency
- Community discussions

---

*"The market doesn't sleep, and neither does Luna."* 🌙

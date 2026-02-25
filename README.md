# PlusE Financial Analysis Skill

AI-ready financial data for your AI agent. Stock analysis, options, sentiment, and predictions—ML-processed so your AI understands it directly.

## Why PlusE?

Traditional financial APIs return massive raw JSON that's slow and expensive for AI to process. PlusE data is ML-preprocessed and AI-optimized.

- **80% fewer tokens** - Data is pre-digested, no parsing needed
- **90% faster** - No 150KB raw data to process
- **50% more accurate** - ML filters out noise

## Installation

### From ClawHub (Recommended)

```bash
npm i -g clawhub
clawhub install plusefin-analysis
```

### Manual

Copy the `plusefin-analysis` folder to your skills directory.

## Configuration

```bash
export PLUSEFIN_API_KEY=your_api_key
```

Or in `~/.openclaw/openclaw.json`:

```json
{
  "skills": {
    "entries": {
      "plusefin-analysis": {
        "enabled": true,
        "apiKey": "your_api_key"
      }
    }
  }
}
```

**Get your free API key**: [console.plusefin.com](https://console.plusefin.com) - No credit card required

## Features

| Feature | Command | Example |
|---------|---------|---------|
| Stock overview | `ticker` | `python {baseDir}/plusefin.py ticker AAPL` |
| Price history | `price-history` | `python {baseDir}/plusefin.py price-history NVDA 1y` |
| Options chain | `options` | `python {baseDir}/plusefin.py options TSLA 20` |
| Financial statements | `statements` | `python {baseDir}/plusefin.py statements AAPL income` |
| Earnings history | `earnings` | `python {baseDir}/plusefin.py earnings NVDA` |
| Market sentiment | `sentiment` | `python {baseDir}/plusefin.py sentiment` |
| Price prediction | `prediction` | `python {baseDir}/plusefin.py prediction AAPL` |
| Economic data | `fred` | `python {baseDir}/plusefin.py fred GDP` |
| Insider trading | `insiders` | `python {baseDir}/plusefin.py insiders NVDA` |

## Pricing

| Plan | Price | Description |
|------|-------|-------------|
| **Trial** | **Free** | Hundreds of calls/month, no credit card |
| Flex | $9.9/750 credits | Pay as you go |
| Trader | $39.9/month | For active traders |

## Links

- [ClawHub](https://clawhub.ai/skills/plusefin-analysis)
- [GitHub](https://github.com/plusefin/plusefin-skill)
- [API Docs](https://mcp.plusefin.com/api/docs)
- [PlusE Website](https://plusefin.com)

## Requirements

- Python 3.x
- PlusE API Key (free)

## License

MIT

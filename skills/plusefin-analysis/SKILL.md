---
name: plusefin-analysis
description: AI-ready stock analysis - ticker data, options, sentiment, predictions. Free tier available!
metadata:
  {
    "openclaw":
      {
        "emoji": "📈",
        "homepage": "https://github.com/plusefin/plusefin-skill",
        "requires": { "bins": ["python3"], "env": ["PLUSEFIN_API_KEY"] },
        "primaryEnv": "PLUSEFIN_API_KEY"
      }
  }
---

# PlusE Financial Analysis

AI-ready financial data for stock analysis, options, and market sentiment. ML-processed data that your AI can understand directly—no raw JSON parsing needed.

**Free Tier**: Hundreds of API calls/month, no credit card required. [Get Started →](https://console.plusefin.com)

## Quick Start

```bash
# 1. Set your API key
export PLUSEFIN_API_KEY=your_api_key

# 2. Start analyzing
python {baseDir}/plusefin.py ticker AAPL
```

## What You Can Do

### Stock Analysis

| Command | What It Does | Example |
|---------|--------------|---------|
| `ticker` | Company overview, valuation, analyst ratings | `python {baseDir}/plusefin.py ticker AAPL` |
| `price-history` | Historical prices + technical signal digest | `python {baseDir}/plusefin.py price-history NVDA 1y` |
| `statements` | Financial statements (income/balance/cash) | `python {baseDir}/plusefin.py statements AAPL income` |
| `earnings` | Earnings history, beats and misses | `python {baseDir}/plusefin.py earnings NVDA` |
| `news` | Stock-related news | `python {baseDir}/plusefin.py news TSLA` |

### Options Analysis

| Command | What It Does | Example |
|---------|--------------|---------|
| `options` | Options chain data | `python {baseDir}/plusefin.py options TSLA 20` |
| `options-analyze` | Options analysis | `python {baseDir}/plusefin.py options-analyze AAPL` |

### Market Sentiment

| Command | What It Does | Example |
|---------|--------------|---------|
| `sentiment` | Current Fear & Greed index | `python {baseDir}/plusefin.py sentiment` |
| `sentiment-history` | Historical sentiment data | `python {baseDir}/plusefin.py sentiment-history 10` |
| `sentiment-trend` | Sentiment trend analysis | `python {baseDir}/plusefin.py sentiment-trend 10` |

### Predictions & Macro

| Command | What It Does | Example |
|---------|--------------|---------|
| `prediction` | ML-based price prediction | `python {baseDir}/plusefin.py prediction AAPL` |
| `fred` | Federal Reserve economic data (GDP, unemployment, etc.) | `python {baseDir}/plusefin.py fred GDP` |
| `fred-search` | Search economic indicators | `python {baseDir}/plusefin.py fred-search unemployment` |

### Holdings & Insider Trading

| Command | What It Does | Example |
|---------|--------------|---------|
| `holders` | Institutional holdings | `python {baseDir}/plusefin.py holders SPY` |
| `top25` | Top 25 holders | `python {baseDir}/plusefin.py top25 AAPL` |
| `insiders` | Insider trading activity | `python {baseDir}/plusefin.py insiders NVDA` |

## Common Workflows

### Deep Dive on a Stock

```
1. Company overview: python {baseDir}/plusefin.py ticker AAPL
2. Check earnings: python {baseDir}/plusefin.py earnings AAPL
3. Financial statements: python {baseDir}/plusefin.py statements AAPL income
4. Recent news: python {baseDir}/plusefin.py news AAPL
5. Summarize with investment thesis
```

### Options Trading Analysis

```
1. Current price: python {baseDir}/plusefin.py ticker TSLA
2. Options chain: python {baseDir}/plusefin.py options TSLA 20
3. Analyze Greeks and implied volatility
```

### Market Overview

```
1. Market sentiment: python {baseDir}/plusefin.py sentiment
2. Macro data: python {baseDir}/plusefin.py fred GDP
3. Assess overall market conditions
```

## Parameters

- `price-history`: period supports `1mo`, `3mo`, `6mo`, `1y`, `2y`, `5y`
- `options`: num is number of options to return (default: 20)
- `statements`: type supports `income`, `balance`, `cash`; frequency supports `quarterly`, `annual`
- `sentiment-history/trend`: days defaults to 10

## Get Your API Key

1. Visit [console.plusefin.com](https://console.plusefin.com)
2. Sign up (free, no credit card)
3. Copy your API key
4. Set environment variable: `export PLUSEFIN_API_KEY=your_key`

## Pricing

| Plan | Price | Description |
|------|-------|-------------|
| **Trial** | **Free** | Hundreds of calls/month, no credit card |
| Flex | $9.9/750 credits | Pay as you go |
| Trader | $39.9/month | For active traders |

## Links

- [GitHub](https://github.com/plusefin/plusefin-skill)
- [ClawHub](https://clawhub.ai/skills/plusefin-analysis)
- [API Docs](https://mcp.plusefin.com/api/docs)
- [PlusE Website](https://plusefin.com)

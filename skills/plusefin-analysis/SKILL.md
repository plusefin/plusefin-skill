---
name: plusefin-analysis
description: Comprehensive financial analysis using PlusE API - stocks, ETFs, options, macro data, and market sentiment
metadata:
  {
    "openclaw":
      {
        "emoji": "📈",
        "homepage": "https://plusefin.com/docs/api/",
        "requires": { "bins": ["python3"], "env": ["PLUSEFIN_API_KEY"] },
        "primaryEnv": "PLUSEFIN_API_KEY"
      }
  }
---

# PlusE Financial Analysis

Access PlusE financial data API for comprehensive stock analysis, ETF holdings, options data, market sentiment, and macroeconomic indicators.

## Setup

Set your PlusE API key as an environment variable:

```bash
export PLUSEFIN_API_KEY=your_api_key
```

Get your API key at [console.plusefin.com](https://console.plusefin.com).

## Available Commands

### Stock Data

| Command | Description | Example |
|---------|-------------|---------|
| `ticker` | Company overview and key metrics | `python {baseDir}/plusefin.py ticker AAPL` |
| `price-history` | Historical price data | `python {baseDir}/plusefin.py price-history NVDA 1y` |
| `statements` | Financial statements | `python {baseDir}/plusefin.py statements AAPL income` |
| `earnings` | Earnings history and surprises | `python {baseDir}/plusefin.py earnings NVDA` |
| `news` | Stock-related news | `python {baseDir}/plusefin.py news TSLA` |

### Holdings & Ownership

| Command | Description | Example |
|---------|-------------|---------|
| `holders` | Institutional holders | `python {baseDir}/plusefin.py holders SPY` |
| `top25` | Top 25 holders | `python {baseDir}/plusefin.py top25 AAPL` |
| `insiders` | Insider trading activity | `python {baseDir}/plusefin.py insiders NVDA` |

### Options

| Command | Description | Example |
|---------|-------------|---------|
| `options` | Options chain data | `python {baseDir}/plusefin.py options TSLA 20` |
| `options-analyze` | Options analysis | `python {baseDir}/plusefin.py options-analyze AAPL` |

### Market Sentiment

| Command | Description | Example |
|---------|-------------|---------|
| `sentiment` | Current market sentiment | `python {baseDir}/plusefin.py sentiment` |
| `sentiment-history` | Historical sentiment | `python {baseDir}/plusefin.py sentiment-history 10` |
| `sentiment-trend` | Sentiment trend analysis | `python {baseDir}/plusefin.py sentiment-trend 10` |

### Predictions & Analysis

| Command | Description | Example |
|---------|-------------|---------|
| `prediction` | Price prediction | `python {baseDir}/plusefin.py prediction AAPL` |

### Macro Data

| Command | Description | Example |
|---------|-------------|---------|
| `fred` | FRED economic data | `python {baseDir}/plusefin.py fred GDP` |
| `fred-search` | Search FRED series | `python {baseDir}/plusefin.py fred-search unemployment` |

### Market News

| Command | Description | Example |
|---------|-------------|---------|
| `news-market` | CNBC market news | `python {baseDir}/plusefin.py news-market` |
| `news-social` | Social media discussions | `python {baseDir}/plusefin.py news-social tsla,nvda` |

## Analysis Workflows

### Comprehensive Stock Analysis

```
1. Get company overview:
   python {baseDir}/plusefin.py ticker AAPL

2. Check earnings history:
   python {baseDir}/plusefin.py earnings AAPL

3. Review financial statements:
   python {baseDir}/plusefin.py statements AAPL income

4. Get recent news:
   python {baseDir}/plusefin.py news AAPL

5. Check institutional ownership:
   python {baseDir}/plusefin.py holders AAPL

6. Summarize with investment thesis
```

### Options Trading Analysis

```
1. Get current stock data:
   python {baseDir}/plusefin.py ticker TSLA

2. Get options chain:
   python {baseDir}/plusefin.py options TSLA 20

3. Run options analysis:
   python {baseDir}/plusefin.py options-analyze TSLA

4. Analyze Greeks, IV, and optimal strikes
```

### Market Overview

```
1. Check market sentiment:
   python {baseDir}/plusefin.py sentiment

2. Get market news:
   python {baseDir}/plusefin.py news-market

3. Check key economic indicators:
   python {baseDir}/plusefin.py fred GDP
   python {baseDir}/plusefin.py fred UNRATE

4. Summarize market conditions
```

### ETF Analysis

```
1. Get ETF overview:
   python {baseDir}/plusefin.py ticker SPY

2. Check holdings:
   python {baseDir}/plusefin.py holders SPY

3. Get top positions:
   python {baseDir}/plusefin.py top25 SPY

4. Analyze sector allocation and risk
```

## Parameters Reference

### price-history
- `ticker`: Stock symbol (required)
- `period`: Time period - "1mo", "3mo", "6mo", "1y", "2y", "5y" (default: "6mo")

### options
- `symbol`: Stock symbol (required)
- `num`: Number of options to return (default: 20)

### statements
- `symbol`: Stock symbol (required)
- `type`: Statement type - "income", "balance", "cash" (default: "income")
- `frequency`: "quarterly" or "annual" (default: "quarterly")

### sentiment-history / sentiment-trend
- `days`: Number of days (default: 10)

### fred-search
- `query`: Search term (required)

### news-social
- `keywords`: Comma-separated keywords (required)

## Error Handling

If you see "Error: PLUSEFIN_API_KEY environment variable not set", make sure to export your API key first.

For HTTP errors, check that:
- Your API key is valid
- The symbol/series_id exists
- You have sufficient API quota

## API Documentation

Full API documentation: https://mcp.plusefin.com/api/docs

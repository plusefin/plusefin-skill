# PlusE Financial Analysis Skill

A comprehensive financial analysis skill for OpenClaw that provides access to PlusE financial data API.

## Features

- **Stock Data**: Company overview, price history, financial statements, earnings
- **Options**: Options chain, Greeks, volatility analysis
- **Holdings**: Institutional holders, top 25 positions, insider trading
- **Market Sentiment**: Fear & Greed index, historical sentiment, trends
- **Predictions**: Price predictions using ML models
- **Macro Data**: FRED economic indicators
- **News**: Market news and social media discussions

## Installation

### Via ClawHub (Recommended)

```bash
# Install ClawHub CLI
npm i -g clawhub

# Install the skill
clawhub install plusefin-analysis
```

### Manual Installation

Copy the `plusefin-analysis` folder to your skills directory:
- Workspace: `<workspace>/skills/`
- Global: `~/.openclaw/skills/`

## Configuration

Set your PlusE API key:

```bash
export PLUSEFIN_API_KEY=your_api_key
```

Or configure in `~/.openclaw/openclaw.json`:

```json
{
  "skills": {
    "entries": {
      "plusefin-analysis": {
        "enabled": true,
        "apiKey": "your_api_key",
        "env": {
          "PLUSEFIN_API_KEY": "your_api_key"
        }
      }
    }
  }
}
```

Get your API key at [console.plusefin.com](https://console.plusefin.com).

## Usage

The skill provides a Python CLI that can be called via the exec tool:

```bash
# Get stock ticker data
python {baseDir}/plusefin.py ticker AAPL

# Get price history
python {baseDir}/plusefin.py price-history NVDA 1y

# Get options chain
python {baseDir}/plusefin.py options TSLA 20

# Get market sentiment
python {baseDir}/plusefin.py sentiment
```

## Available Commands

| Category | Commands |
|----------|----------|
| Stock Data | `ticker`, `price-history`, `statements`, `earnings`, `news` |
| Holdings | `holders`, `top25`, `insiders` |
| Options | `options`, `options-analyze` |
| Sentiment | `sentiment`, `sentiment-history`, `sentiment-trend` |
| Predictions | `prediction` |
| Macro | `fred`, `fred-search` |
| News | `news-market`, `news-social` |

## Requirements

- Python 3.x
- `PLUSEFIN_API_KEY` environment variable

## API Documentation

- Full API docs: https://mcp.plusefin.com/api/docs
- PlusE documentation: https://plusefin.com/docs/api/

## License

MIT

# PlusE Financial Analysis Skill

AI-ready financial data for your AI agent. Stock analysis, options, sentiment, and predictions—ML-processed so your AI understands it directly.

## Why PlusE?

Traditional financial APIs return massive raw JSON that's slow and expensive for AI to process. PlusE data is ML-preprocessed and AI-optimized.

- **80% fewer tokens** - Data is pre-digested, no parsing needed
- **90% faster** - No 150KB raw data to process
- **50% more accurate** - ML filters out noise

## Cross-Platform Compatibility

This skill works on all major AI coding agents:

| Platform | Skill Location | Method |
|----------|---------------|--------|
| **Claude Code** | `.claude/skills/plusefin-analysis/` | MCP or CLI |
| **OpenCode** | `.opencode/skills/plusefin-analysis/` | MCP or CLI |
| **Codex CLI** | `.agents/skills/plusefin-analysis/` | CLI or curl |

## Installation

### From ClawHub (Recommended)

```bash
npm i -g clawhub
clawhub install plusefin-analysis
```

### Manual (Cross-Platform)

Choose your platform's location:

```bash
# For Claude Code
cp -r skills/plusefin-analysis .claude/skills/

# For OpenCode
cp -r skills/plusefin-analysis .opencode/skills/

# For Codex CLI (also works with Claude/OpenCode)
cp -r skills/plusefin-analysis .agents/skills/
```

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

## Quick Start

```bash
# CLI mode
export PLUSEFIN_API_KEY=your_api_key
python skills/plusefin-analysis/plusefin.py ticker AAPL

# Or curl mode
curl -s -H "Authorization: Bearer $PLUSEFIN_API_KEY" \
  https://mcp.plusefin.com/api/tools/ticker/AAPL
```

## Available Data

| Category | Commands |
|----------|----------|
| Company Fundamentals | `ticker`, `price-history`, `statements`, `earnings`, `news` |
| Options | `options-analyze`, `options` |
| Institutional Activity | `top25`, `holders`, `insiders` |
| Market Sentiment | `sentiment`, `sentiment-history`, `sentiment-trend` |
| Macro Data | `fred`, `fred-search` |
| News | `news-market`, `news-social` |
| Predictions | `prediction` |

## Pricing

| Plan | Price | Description |
|------|-------|-------------|
| **Trial** | **Free** | Hundreds of calls/month, no credit card |
| Flex | $9.9/750 credits | Pay as you go |
| Trader | $39.9/month | For active traders |

## Links

- [ClawHub](https://clawskills.sh/skills/wanghsinche-plusefin-analysis)
- [GitHub](https://github.com/plusefin/plusefin-skill)
- [API Docs](https://mcp.plusefin.com/api/docs)
- [PlusE Website](https://plusefin.com)

## Requirements

- Python 3.x
- PlusE API Key (free)

## License

MIT

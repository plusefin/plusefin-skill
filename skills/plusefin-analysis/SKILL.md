---
name: plusefin-analysis
description: AI-ready stock analysis with financial data, options, sentiment, and structured research framework
metadata:
  clawdbot:
    emoji: "📈"
    homepage: "https://github.com/plusefin/plusefin-skill"
    requires:
      env: ["PLUSEFIN_API_KEY"]
    primaryEnv: "PLUSEFIN_API_KEY"
---

# PlusE Financial Analysis

AI-ready financial data research skill with structured research methodology.

## Setup

```bash
export PLUSEFIN_API_KEY=your_api_key
```

## Research Framework

### 1. Research Setup
- Define target (ticker) and time range (6mo / 1y / 2y)
- Set research objective: valuation analysis / technical outlook / event-driven

### 2. Data Collection
- **Company Fundamentals**: `ticker` - overview, valuation, ratings
- **Market Sentiment**: `sentiment` / `sentiment-history`
- **Options Data**: `options` / `options-analyze` (IV, Greeks, OI)
- **Institutional Holdings**: `holders` - major holders changes
- **Financial Statements**: `statements` (income/balance/cash)
- **Earnings & Insider**: `earnings` / `insiders`
- **Price History**: `price-history`

### 3. Hypothesis Formation
Based on data, formulate hypotheses:
- **Direction**: Bullish / Bearish / Neutral
- **Drivers**: Valuation reversion, earnings growth, event catalyst, sentiment reversal

### 4. Evidence Validation
- Use search capabilities to gather research reports, news, announcements
- Cross-validate multi-source data timeline consistency
- Seek evidence supporting or refuting hypotheses

### 5. Valuation Scenarios
- **Bull Case**: Valuation assuming upside catalysts materialize
- **Base Case**: Valuation based on current market expectations
- **Bear Case**: Valuation assuming downside risks materialize

### 6. Risk Assessment
- Downside risks
- Key assumption risks
- Potential catalysts and triggers

### 7. Report Output
Structured output:
- Core thesis
- Evidence summary
- Valuation scenario comparison
- Risk warnings
- Actionable recommendations (if applicable)

Each key conclusion must include source citations.

## Commands

| Command | Description |
|---------|-------------|
| `ticker` | Company overview, valuation, ratings |
| `price-history` | Historical prices and signals |
| `sentiment` | Market sentiment (Fear & Greed) |
| `sentiment-history` | Historical sentiment data |
| `options` | Options chain |
| `options-analyze` | Options analysis |
| `holders` | Institutional holdings |
| `statements` | Financial statements |
| `earnings` | Earnings history |
| `insiders` | Insider trading |
| `news` | Stock news |
| `fred` | Macroeconomic data |

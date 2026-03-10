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

### 1. 研究准备
- 明确标的（股票代码）和时间范围（6mo / 1y / 2y）
- 设定研究目标：估值分析 / 技术面判断 / 事件驱动

### 2. 数据收集
- **公司基本面**：`ticker` 获取概览、估值、评级
- **市场情绪**：`sentiment` / `sentiment-history` 
- **期权数据**：`options` / `options-analyze` (IV、Greeks、OI)
- **机构持仓**：`holders` 头部机构变动
- **财务数据**：`statements` (income/balance/cash)
- **盈利与内幕**：`earnings` / `insiders`
- **价格历史**：`price-history`

### 3. 假设形成
基于数据提出猜想：
- **方向判断**：看多 / 看空 / 中性
- **驱动逻辑**：估值修复、业绩增长、事件催化、情绪反转

### 4. 证据验证
- 使用搜索能力获取权威研报、新闻、公告
- 交叉验证多源数据时间线一致性
- 寻找支持或反驳假设的证据

### 5. 估值情景分析
- **乐观情景**：假设利好兑现的估值
- **中性情景**：当前市场预期的估值  
- **悲观情景**：假设利空兑现的估值

### 6. 风险评估
- 下行风险点
- 关键假设风险
- 潜在催化剂与触发因素

### 7. 报告输出
结构化输出：
- 核心观点
- 证据链摘要
- 估值情景对比
- 风险提示
- 操作建议（如适用）

每条关键结论需附来源引用。

## Commands

| Command | Description |
|---------|-------------|
| `ticker` | 公司概览、估值、评级 |
| `price-history` | 历史价格与信号 |
| `sentiment` | 市场情绪（Fear & Greed） |
| `sentiment-history` | 历史情绪数据 |
| `options` | 期权链 |
| `options-analyze` | 期权分析 |
| `holders` | 机构持仓 |
| `statements` | 财务报表 |
| `earnings` | 盈利历史 |
| `insiders` | 内幕交易 |
| `news` | 股票新闻 |
| `fred` | 宏观经济数据 |

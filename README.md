# PlusE Financial Analysis Skill

让 AI 帮你分析股票、期权、市场情绪。

## 为什么用这个？

传统金融 API 返回一堆原始 JSON，AI 处理起来又慢又费 token。PlusE 的数据经过 ML 预处理，AI 直接能懂。

- **80% token 减少** - 数据已经整理好，不用 AI 自己解析
- **90% 更快** - 不用处理 150KB 的原始数据
- **50% 更准** - ML 过滤噪音信号

## 安装

### 从 ClawHub 安装（推荐）

```bash
npm i -g clawhub
clawhub install plusefin-analysis
```

### 手动安装

复制 `plusefin-analysis` 文件夹到你的 skills 目录。

## 配置

```bash
# 设置 API Key
export PLUSEFIN_API_KEY=your_api_key
```

或在 `~/.openclaw/openclaw.json` 中配置：

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

**免费获取 API Key**：[console.plusefin.com](https://console.plusefin.com) - 无需信用卡

## 能做什么

| 功能 | 命令 | 例子 |
|------|------|------|
| 股票概况 | `ticker` | `python {baseDir}/plusefin.py ticker AAPL` |
| 历史价格 | `price-history` | `python {baseDir}/plusefin.py price-history NVDA 1y` |
| 期权链 | `options` | `python {baseDir}/plusefin.py options TSLA 20` |
| 财务报表 | `statements` | `python {baseDir}/plusefin.py statements AAPL income` |
| 财报历史 | `earnings` | `python {baseDir}/plusefin.py earnings NVDA` |
| 市场情绪 | `sentiment` | `python {baseDir}/plusefin.py sentiment` |
| 价格预测 | `prediction` | `python {baseDir}/plusefin.py prediction AAPL` |
| 经济数据 | `fred` | `python {baseDir}/plusefin.py fred GDP` |
| 内幕交易 | `insiders` | `python {baseDir}/plusefin.py insiders NVDA` |

## 定价

| 方案 | 价格 | 说明 |
|------|------|------|
| **Trial** | **免费** | 数百次调用/月，无需信用卡 |
| Flex | $9.9/750 credits | 按需付费 |
| Trader | $39.9/月 | 高频交易者 |

## 链接

- [ClawHub 页面](https://clawhub.ai/skills/plusefin-analysis)
- [GitHub](https://github.com/plusefin/plusefin-skill)
- [API 文档](https://mcp.plusefin.com/api/docs)
- [PlusE 官网](https://plusefin.com)

## 要求

- Python 3.x
- PlusE API Key（免费）

## License

MIT

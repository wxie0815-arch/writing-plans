# ✍️ Writing Plans — 结构化写作计划生成 Skill

[![Version](https://img.shields.io/badge/version-1.1.0-blue)](https://github.com/wxie0815-arch/writing-plans)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Compatible-green)](https://openclaw.ai)
[![License](https://img.shields.io/badge/license-MIT-orange)](LICENSE)

> 将模糊的创作意图转化为清晰、结构化的写作计划。支持注入市场数据、链上指标等外部上下文，专为加密货币内容创作优化。

## 🎯 功能概述

`writing-plans` 是三阶段专业写作流程的**第一阶段**，负责将用户的创作意图转化为可执行的结构化写作计划（JSON格式大纲）。

```
writing-plans  →  copywriting  →  humanizer-zh
   (规划阶段)       (撰写阶段)      (优化阶段)
```

## ✨ 核心特性

- **结构化输出**：生成标准 JSON 格式的写作计划，可直接被 `copywriting` skill 使用
- **上下文感知**：支持注入市场数据、热门话题、链上指标等外部数据，生成更专业的内容
- **风格指纹融合**：支持注入用户历史写作风格，确保输出文章风格一致性
- **多场景适配**：支持加密市场分析、项目研究、教程科普、KOL观点等多种内容类型
- **零配置**：自动使用 OpenClaw 环境中的 LLM 配置，无需额外设置

## 🚀 快速开始

### 安装

```bash
gh repo clone wxie0815-arch/writing-plans
```

### 在 binance-square-oracle 中使用

`writing-plans` 已内置于 [binance-square-oracle](https://github.com/wxie0815-arch/binance-square-oracle) 预言机中，通过三阶段写作流程自动调用：

```python
from L7_article_generator import generate_article_v3

result = generate_article_v3(
    l0_result=market_data,
    l6_fingerprint=style_fingerprint,
    user_intent="写一篇关于Layer2发展趋势的分析文章"
)
```

### 独立使用

```python
from writing_skill import WritingSkill

skill = WritingSkill()
plan = skill.generate_writing_plan(
    intent="写一篇关于BTC突破新高的分析文章",
    context={
        "top_tokens": ["BTC", "ETH"],
        "market_sentiment": "偏多",
        "hot_topics": ["Layer2", "ETF"]
    }
)
print(plan)
```

## 📋 输出格式

```json
{
  "core_argument": "核心论点（一句话）",
  "target_audience": "目标受众描述",
  "key_points": ["要点1", "要点2", "要点3"],
  "structure": {
    "introduction": "引言策略",
    "body": ["正文段落1", "正文段落2"],
    "conclusion": "结论策略"
  },
  "content_suggestions": {
    "data": "建议引用的数据",
    "cases": "建议引用的案例",
    "style": "建议的写作风格"
  },
  "estimated_length": "800-1200字"
}
```

## 🔗 相关 Skill

| Skill | 说明 | 仓库 |
|-------|------|------|
| `copywriting` | 根据写作计划撰写文案初稿 | [wxie0815-arch/copywriting](https://github.com/wxie0815-arch/copywriting) |
| `humanizer-zh` | 去除AI味，优化中文表达 | [wxie0815-arch/humanizer-zh](https://github.com/wxie0815-arch/humanizer-zh) |
| `binance-square-oracle` | 集成三阶段写作的完整预言机 | [wxie0815-arch/binance-square-oracle](https://github.com/wxie0815-arch/binance-square-oracle) |

## 📄 许可证

MIT License — 自由使用、修改和分发。

---

## 💰 赞助支持

如果这个项目对您有帮助，欢迎赞助支持！

**BSC（BEP-20）钱包地址：**
 

支持 USDT / BNB / 任意 BEP-20 代币。感谢每一位支持者 🙏

**作者：** 无邪Infinity | 币安广场 [@wuxie](https://www.binance.com/en/square/profile/wuxie) | X [@wuxie149](https://x.com/wuxie149)

---

## 💰 赞助支持

如果这个项目对您有帮助，欢迎赞助支持！

**BSC（BEP-20）钱包地址：**
 

支持 USDT / BNB / 任意 BEP-20 代币。感谢每一位支持者 🙏

**作者：** 无邪Infinity | 币安广场 [@wuxie](https://www.binance.com/en/square/profile/wuxie) | X [@wuxie149](https://x.com/wuxie149)

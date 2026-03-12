# ✍️ Writing Plans — 结构化写作计划生成 Skill

[![Version](https://img.shields.io/badge/version-1.1.0-blue)](https://github.com/wxie0815-arch/writing-plans)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Compatible-green)](https://openclaw.ai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

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

`writing-plans` 已内置于 [binance-square-oracle](https://github.com/wxie0815-arch/binance-square-oracle) 预言机中，通过三阶段写作流程自动调用。

### 独立使用

详细的 Prompt 指令、输入输出格式和示例，请参考 `SKILL.md`。

## 🔗 相关 Skill

| Skill | 说明 | 仓库 |
|-------|------|------|
| `copywriting` | 根据写作计划撰写文案初稿 | [wxie0815-arch/copywriting](https://github.com/wxie0815-arch/copywriting) |
| `humanizer-zh` | 去除AI味，优化中文表达 | [wxie0815-arch/humanizer-zh](https://github.com/wxie0815-arch/humanizer-zh) |
| `binance-square-oracle` | 集成三阶段写作的完整预言机 | [wxie0815-arch/binance-square-oracle](https://github.com/wxie0815-arch/binance-square-oracle) |

## 📄 许可证

MIT License

---

## 💰 赞助支持

如果这个项目对您有帮助，欢迎赞助支持！

**BSC（BEP-20）钱包地址：**
`0x3B74BE938caB987120C3661C8e3161CD838e5a1A` 

支持 USDT / BNB / 任意 BEP-20 代币。感谢每一位支持者 🙏

**作者：** 无邪Infinity | 币安广场 [@wuxie](https://www.binance.com/en/square/profile/wuxie) | X [@wuxie149](https://x.com/wuxie149)

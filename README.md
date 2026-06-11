# 快递单号提取器 v2

> 一个纯前端的快递单号批量提取工具，支持文字粘贴和截图 AI 识别，无需后端，开箱即用。

![License](https://img.shields.io/badge/license-MIT-blue)
![HTML](https://img.shields.io/badge/HTML-单文件-orange)
![AI](https://img.shields.io/badge/AI-OCR识别-green)

---

## ✨ 功能特性

- **文字模式**：将微信群/钉钉消息整段粘贴，自动提取所有快递单号，不消耗任何 API 费用
- **截图模式**：上传快递面单、聊天截图，由 AI 视觉模型识别单号，支持模糊、复杂背景
- **自动去重**：多次提取结果自动合并去重
- **一键导出**：结果导出为 Excel（CSV）文件，带序号
- **多模型支持**：gpt-4o-mini / gpt-4o / claude-haiku / claude-sonnet，按需选择精度和成本
- **纯本地运行**：代码完全在浏览器执行，图片不上传服务器，数据安全

---

## 🚀 快速使用

### 方式一：直接下载使用

下载 `index.html`，用浏览器打开即可，无需安装任何依赖。

### 方式二：在线体验

在线地址：jotarou.com/tools/express
备用地址：jotaroustar.github.io/express-number-extractor

---

## 🔑 截图识别需要 API Key

文字提取模式完全免费，无需 Key。

截图 AI 识别功能需要填入 API Key，推荐使用 **[Jotarou API](https://jotarou.com)**：

- 支持 GPT-4o / Claude / DeepSeek 等模型
- 支付宝充值，按量计费，无月费
- 注册即送 ¥7 试用额度，足够识别 200+ 张截图

```
Base URL: https://jotarou.com
注册地址: https://jotarou.com/register
```

当然也可以填入官方 OpenAI / Anthropic 的 Key，工具完全兼容。

---

## 📦 支持的单号格式

| 类型 | 示例 | 说明 |
|------|------|------|
| 字母前缀型 | `YT1234567890123` | 圆通、韵达等 |
| 纯数字型 | `123456789012345` | 顺丰、京东等 |
| 混合型 | `SF1234567890` | 顺丰特殊格式 |

最短位数可调（10-13位），过滤误识别的短数字。

---

## 💰 费用参考

| 模型 | 每张截图费用 | 适用场景 |
|------|------------|---------|
| gpt-4o-mini | ¥0.01~0.03 | 日常使用，推荐 |
| gpt-4o | ¥0.05~0.15 | 图片模糊/复杂时 |
| claude-haiku-4-5 | ¥0.02~0.05 | 速度快，备选 |
| claude-sonnet-4-6 | ¥0.10~0.25 | 最高精度 |

---

## 🛠️ 技术栈

- 纯 HTML + CSS + JavaScript，零依赖
- 调用 OpenAI 兼容接口（vision 功能）
- 正则 + AI 双引擎提取，互为补充

---

## 📁 文件结构

```
.
└── index.html   # 全部代码，单文件
```

---

## 📄 License

MIT License · 自由使用、修改、分发

---

## 🔗 相关项目

| 项目 | 说明 |
|------|------|
| [Jotarou API](https://jotarou.com) | 本工具推荐使用的 AI API 中转服务 |
| 更多工具持续开发中… | GitHub 主页关注更新 |

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/jotaroustar">jotaroustar</a>
</p>

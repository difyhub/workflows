# DifyHub 工作流库

[一个由社区驱动的、即插即用的 Dify 工作流库。](https://dify.ai)
<br />
在这里查找、分享和提交你的 Dify DSL 工作流文件。
<br />
<br />
由 [**DifyHub.com**](https://difyhub.com) 提供支持 —— 浏览和部署 Dify 工作流的最佳平台。
<br />
<br />
[**English README (英文文档)**](https://github.com/difyhub/workflows/blob/main/README.md)

---

## 什么是 DifyHub？

DifyHub 是一个面向 Dify 工作流的开源社区和平台。本仓库存储了所有在 [DifyHub.com](https://difyhub.com) 网站（即将上线！）上展示的工作流的 DSL 文件和元数据。

我们的目标是创建一个“中心枢纽”，任何人都可以从中找到高质量、经过实战测试的工作流，为你的 Dify 应用赋能，节省你从零开始构建的宝贵时间。

*(发起人寄语：大家好，我是独孤风。作为一名 AI 全栈工程师，我深知构建高质量工作流的价值和挑战。我发起了 DifyHub 这个项目，希望能和社区一起，打造一个最好用的工作流“军火库”。)*

## 📚 工作流总览

点击下方的工作流标题即可进入对应目录，查看 README、使用截图以及部署指引。

### 数据分析

| 工作流 | 说明 |
| --- | --- |
| [Smart Chart Generator (EN)](data-analysis/smart-chart-generator-en/README.md) | Excel/CSV 数据上传后，借助 DeepSeek Coder 自动生成可交互的 ECharts HTML 图表。 |
| [智能图表生成助手 (CN)](data-analysis/smart-chart-generator-cn/README.md) | 中文提示词与界面，上传表格即可一键产出可交互的 ECharts 页面。 |
| [Text-to-SQL Data Analyst (EN)](data-analysis/text-to-sql-en/README.md) | 将英文自然语言问题转成 SQL，调用自建 HTTP API 执行并输出图表化洞察。 |
| [Text-to-SQL 数据分析师 (CN)](data-analysis/text-to-sql-cn/README.md) | 中文 Text-to-SQL 模板，适合需要自建数据库/API 的进阶场景。 |

### 文本处理

| 工作流 | 说明 |
| --- | --- |
| [Basic Text Summarizer (EN)](text-processing/basic-text-summarizer-en/README.md) | 英文长文本自动摘要，适合新手快速上手 Dify 工作流。 |
| [基础文本摘要器 (CN)](text-processing/basic-text-summarizer-cn/README.md) | 中文摘要版本，支持一段话输入、直接输出精炼摘要。 |

### 图像生成

| 工作流 | 说明 |
| --- | --- |
| [FLUX Painting Robot (EN)](image-generation/flux-painter-en/README.md) | 英文绘画请求 → Qwen 提示词优化 → SiliconFlow FLUX.1-schnell 出图。 |
| [FLUX 绘画机器人 (CN)](image-generation/flux-painter-cn/README.md) | 中文需求自动翻译并优化为英文 Flux.1 提示词，再通过 Python 工具链完成出图。 |

### 视觉理解

| 工作流 | 说明 |
| --- | --- |
| [Image Recognition (EN)](vision/image-recognition-en/README.md) | 上传图片，调用 Qwen2.5-VL-32B-Instruct 输出英文描述。 |
| [图片识别 (CN)](vision/image-recognition-cn/README.md) | 中文交互的图片问答模板，可输出简洁准确的中文描述。 |
| [Menu OCR to Excel (菜谱识别)](vision/smart-recipe-recognition/README.md) | 上传菜谱照片自动提取菜名/价格并生成可下载的 Excel，基于多模态识别与 JSON→Excel 链路（推荐 Gemini）。 |

## 🚀 如何使用

1.  **浏览** `/workflows` 目录，找到你需要的工作流。
2.  **打开** `workflow.dsl` 文件。
3.  **复制** 完整的 JSON/YAML 内容，并导入到你的 Dify 应用中。
4.  **(即将上线)** 在 [DifyHub.com](https://difyhub.com) 网站上直观地浏览、搜索和预览所有工作流！

## 💡 如何贡献 (我们需要你！)

我们欢迎所有形式的贡献！如果你构建了一个有用的 Dify 工作流，请务必与社区分享。

**在提交 PR (Pull Request) 之前，请务必阅读我们的贡献指南：**

* **[贡献指南 (CONTRIBUTING_CN.md)](CONTRIBUTING_CN.md)** (中文版)
* **[CONTRIBUTING.md (English Guide)](CONTRIBUTING.md)** (英文版)

## 许可证

本仓库中的所有工作流均基于 **[MIT 许可证](LICENSE)** 发布。

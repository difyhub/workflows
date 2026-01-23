# Menu OCR to Excel (菜谱识别转Excel)

这是一个基于 Dify 的智能工作流，旨在解决餐厅菜单数字化录入的难题。它能将拍摄的**菜谱图片**自动识别、提取信息，并最终生成可直接下载的 **Excel 表格**。

This is a Dify-based intelligent workflow designed to solve the problem of digitizing restaurant menus. It automatically recognizes and extracts information from **menu photos** and converts them into a downloadable **Excel spreadsheet**.

## 📸 预览 (Screenshots)

<!-- 请上传你的截图后，保留下面的格式，但确保图片文件名与你上传的一致 -->
<!-- Upload your images to this folder and ensure filenames match below -->

### 工作流编排 (Workflow Orchestration)
![Workflow Graph](img/workflow_graph.png)

### 运行效果 (Demo)
![Demo Result](img/demo_result.png)

## ✨ 功能特点 (Features)

*   **📷 高精度 OCR (High-Precision OCR)**: 使用多模态大模型 (Gemini 3 Flash Preview) 进行视觉识别，能够精准提取菜名、价格及备注信息。
*   **🧠 智能语义理解 (Intelligent Understanding)**: 提示词经过专门优化，能够识别括弧内的配菜说明、口味备注，绝不遗漏细节。
*   **📊 自动格式化 (Auto Formatting)**: 将非结构化的图片文本自动转换为标准的 JSON 格式。
*   **📥 一键导出 Excel (Direct Excel Export)**: 最终直接输出 Excel 文件链接，无需人工复制粘贴，下载即用。

## 🛠️ 工作流逻辑 (How it works)

1.  **Start**: 接收用户上传的菜谱图片。
2.  **LLM (Gemini 3 Flash Preview)**: 扮演严谨的 OCR 数据录入员，分析图片内容，按严格的 JSON 格式提取数据（包含菜名、价格、详细备注）。
3.  **Code Execution**: 对 LLM 输出的数据进行清洗和校验，确保格式符合转换要求。
4.  **JSON 转 Excel**: 将标准化的数据流转换为 `.xlsx` 文件。
5.  **Direct Reply**: 返回 Excel 文件的下载链接。

## 🚀 如何使用 (Usage)

1.  **导入 DSL**: 下载本仓库的 `.yml` 文件并导入 Dify。
2.  **配置模型**: 确保你的 Dify 环境中已配置支持视觉识别的模型（推荐 **Google Gemini 1.5 Flash/Pro** 或 **Gemini 3 Flash**，识别速度快且成本低）。
3.  **运行**: 点击运行，上传一张清晰的菜谱图片。
4.  **下载**: 等待片刻，点击对话框返回的链接下载 Excel 文件。

## ⚠️ 注意事项 (Notes)

*   请确保上传的图片文字清晰可见。
*   本工作流依赖多模态模型（Vision Model），请确保所选模型支持图片输入。

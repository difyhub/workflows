# 基础文本摘要器

**Author:** `dugufeng`
**Tags:** `language:chinese`, `example`, `beginner`, `text-processing`, `llm`
**Dify Version:** `v1.9.2+` (请填写你测试通过的 Dify 版本)

一个简单的中文工作流，输入一段长文本，返回精炼的中文摘要。

## 🚀 如何使用

1.  **设置 API 密钥:**
    * 此工作流使用 Dify 默认的 LLM 供应商。
    * 请确保你已在 Dify 的“凭据”中设置了有效的 API 密钥 (如 `OPENAI_API_KEY`)。
2.  **运行工作流:**
    * 在“开始”节点的 `text` 变量中提供你想要摘要的中文长文本。
    * 运行工作流，并在“结束”节点查看 `summary` 输出。

## 🛠️ 工作流节点

* **开始节点:** 接收输入的 `text` (段落)。
* **LLM 节点:** 一个大语言模型调用，使用**中文提示词 (Prompt)**，例如：
  `请对以下文本进行精炼的中文摘要：\n\n{{text}}`
* **结束节点:** 返回输出的 `summary` (字符串)。

## 📸 工作流截图 (推荐)
![工作流图](screenshot-workflow.png)

## 📸 运行截图 (推荐)
![运行示例](screenshot-run.png)

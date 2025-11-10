# 图片识别 (Image Recognition)

**Author:** `dugufeng`
**Tags:** `language:chinese`, `example`, `vision`, `multimodal`, `qwen-vl`
**Dify Version:** `v1.9.2+`

一个简单的多模态工作流，输入一张图片，使用 Qwen-VL 模型返回对图片的中文描述。

## ✨ 核心特性

* 支持多模态图像输入，自动生成中文描述。
* 基于 Qwen2.5-VL-32B-Instruct 模型，具备强大的视觉理解能力。
* 无需额外工具配置，开箱即用。

## 🚀 如何使用

1.  **设置 API 密钥:**
    * 此工作流依赖 `langgenius/siliconflow` 供应商。
    * 请确保你已在 Dify 的“凭据”中为 SiliconFlow (或相关供应商) 设置了有效的 API 密钥。
2.  **配置工具:**
    * 无需配置额外工具。
3.  **运行工作流:**
    * 在“开始”节点的 `imageUrl` 变量中**上传一张图片**。
    * 运行工作流，并在“结束”节点查看 `text` 输出（即图片描述）。

## 🛠️ 工作流节点

* **开始节点:** 接收一个 `file` (文件) 类型的输入，变量名为 `imageUrl`。
* **LLM 节点:**
    * 使用 `Qwen/Qwen2.5-VL-32B-Instruct` 多模态模型。
    * 开启了“视觉 (vision)”功能，并将 `imageUrl` 变量传入。
    * **Prompt (中文):** "提取图片核心信息，用简洁准确的语言输出图片内容描述..."
* **结束节点:** 返回一个 `text` (字符串) 类型的输出，即 LLM 生成的描述。

## 📸 运行截图 (强烈推荐)

### 工作流图
(请将你的 `screenshot-workflow.png` 拖放到这里)
`![工作流图](screenshot-workflow.png)`

### 运行示例
(请将你的 `screenshot-run.png` 拖放到这里)
`![运行示例](screenshot-run.png)`

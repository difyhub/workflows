# Image Recognition (English)

**Author:** `dugufeng`
**Tags:** `language:english`, `vision`, `multimodal`, `qwen-vl`, `siliconflow`

This is a straightforward multimodal workflow. It receives an uploaded image and uses the **Qwen2.5-VL-32B-Instruct** model to return a concise description of the image in English.

---

## 🛠️ 关键元数据 (Technical Details)

* **Dify Version:** `v1.9.0+` (Please fill in the Dify version you have tested)

---

## 🚀 关键前置条件 (Pre-conditions)

**1. SiliconFlow API Key:**
* This workflow relies on the `langgenius/siliconflow` provider.
* Please ensure you have configured a valid API Key for SiliconFlow in your Dify "Credentials".

## 🚀 如何使用

1.  **Set API Keys:**
    * Ensure your SiliconFlow API Key is correctly set up in Dify's "Credentials".
2.  **Configure Tools:**
    * No other tools need configuration.
3.  **Run the Workflow:**
    * In the "Start" node's `imageUrl` variable, **upload an image** (or provide a URL).
    * Run the workflow and check the "End" node for the `text` output (the image description).

## 🛠️ 工作流节点 (Optional)

* **Start Node:** Receives a `file` type input named `imageUrl`.
* **LLM (Vision) Node:**
    * Uses `Qwen/Qwen2.5-VL-32B-Instruct` model with `vision` enabled.
    * Receives the `imageUrl` as context.
    * Uses an English System Prompt (see above) to generate a concise description.
* **End Node:** Outputs the final `text` (string) description.

## 📸 运行截图 (Highly Recommended)

### 工作流图
![Workflow Graph](screenshot-workflow.png)

### 运行示例
![Example Run](screenshot-run.png)
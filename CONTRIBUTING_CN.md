
# 如何为 DifyHub 工作流库做出贡献

首先，非常感谢你考虑为社区做出贡献！正是你的贡献，让 DifyHub 成为了一个对 Dify 社区极具价值的资源。

我们欢迎所有高质量的工作流提交。为了确保审核流程的顺畅并保持库的质量，请你遵循以下指南。

(英文版指南请见 [CONTRIBUTING.md](CONTRIBUTING.md))

## 提交一个新的工作流

所有新的工作流都必须通过 **Pull Request (PR)** 来提交。

### 1. 仓库目录结构

本仓库按“类别”组织。请将你的工作流放在 `/workflows` 目录下最相关的子目录中。

- **正确的示例：** `workflows/social-media/ai-tweet-generator` (社交媒体/AI推文生成器)
- **正确的示例：** `workflows/rag/qdrant-pdf-qa` (RAG/Qdrant-PDF问答)
- **错误的示例：** `workflows/my-awesome-workflow` (我的牛X工作流)

如果你不确定该放在哪个类别，请随时创建一个你认为合理的新类别目录。

### 2. 必须包含的文件

你提交的每一个工作流（即你的新文件夹）**必须**包含：

1.  workflow.yml:

    这是从你的 Dify 应用中导出的原始文件。

    [重要!] 你必须将导出的文件（例如 My Workflow.yml 或 我的工作流.yml）重命名为 workflow.yml。

    这能确保用户下载后可直接导入 Dify，同时也能让我们的自动化系统正常工作。
2.  `README.md`: 一个解释你的工作流的 Markdown 文件 (必须使用我们的模板)。

**我们强烈推荐你额外包含：**

3.  `screenshot-workflow.png`: Dify UI 中的工作流节点图（逻辑图）。
4.  `screenshot-run.png`: "调试与预览" 面板的截图，展示输入和输出的示例（结果图）。

### 3. `README.md` 模板 (强制使用)

你的 `README.md` 是你工作流的“说明书”。它必须清晰易懂。请 **复制并粘贴以下模板** 到你的 `README.md` 文件中，并填写完整。

**特别注意：`Tags:` 这一行是必填项。**

```markdown
# [工作流名称]

**Author:** `[你的 GitHub 用户名]`
**Tags:** `language:chinese | language:english`, `标签2`, `标签3`
**Dify 版本:** `v1.9.2+` (请填写你测试通过的 Dify 版本)

(用一句话简短描述这个工作流是做什么的。)

## 🚀 如何使用

1.  **设置 API 密钥:**
    * 这个工作流需要以下 API 密钥 (例如 `OPENAI_API_KEY`)。
    * 请解释去哪里获取它们，以及如何在 Dify 的“凭据”部分添加它们。
2.  **配置工具:**
    * 用户是否需要配置任何工具，比如一个数据库连接或谷歌搜索 API？
3.  **运行工作流:**
    * 解释如何测试它 (例如："在‘开始’节点的 'input' 变量中提供一个 URL...")。

## 🛠️ 工作流节点 (可选，但推荐)

简要概述主要节点及其作用：

* **开始节点:** 接受用户查询 (字符串)。
* **LLM 节点:** 总结输入内容。
* **结束节点:** 返回总结结果。

## 📸 运行截图 (强烈推荐)

### 工作流图
(请将你的 `screenshot-workflow.png` 拖放到这里)

### 运行示例
(请将你的 `screenshot-run.png` 拖放到这里)

关于 Tags (标签):

    language: (必填项): 你 必须 包含 language:chinese 或 language:english 中的一个。

    其他标签: 请添加其他相关的标签 (例如: rag, social-media, beginner, llm, RAG, 社交媒体, 入门)。

### 4. 提交检查清单

在你提交 PR 之前，请确认：

    [ ] 你的工作流能否正常运行？

    [ ] 你的 workflow.dsl 文件是原始导出的（不是复制粘贴的文本）？

    [ ] 你的 README.md 是否使用了模板，并包含了必填的 language: 标签？

    [ ] (推荐) 你是否同时包含了 screenshot-workflow.png 和 screenshot-run.png 两个截图？

    [ ] 你是否已将你的工作流放在了一个合乎逻辑的分类文件夹中？

### 5. 审核流程

    提交 PR: 提交你的 PR 到我们的 main 分支。

    审核: 我们的团队 (@dugufeng 等) 将会审核你的提交。我们可能会要求你进行一些修改。

    合并: 一旦审核通过，你的 PR 将被合并。

    同步: 合并后，你的工作流将被自动同步并发布到 DifyHub.com 网站上！

    感谢你与我们一起共建 Dify 社区！
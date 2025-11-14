# Text-to-SQL Data Analyst

**Author:** `dugufeng`
**Tags:** `language:english`, `text-to-sql`, `database`, `mysql`, `deepseek-coder`, `kimi`, `echarts`

This is an advanced workflow that acts as a "Data Analyst". It converts a user's natural language question (based on a sample database) into SQL, executes the query, and then uses a large model to analyze the raw data and summarize it into a report, complete with ECharts.

---

## 🛠️ 关键元数据 (Technical Details)

* **Dify Version:** `v1.9.0+` (Please fill in the Dify version you have tested)

---

## 🚀 关键前置条件 (Pre-conditions)

**Warning: This is an advanced workflow template. You MUST set up your own database and API to run it.**

Before running this workflow, you **MUST** have the following two environments ready:

1.  **MySQL Database & `employees` Dataset:**
    * You need a running MySQL database.
    * You must import the `employees` sample dataset into this database.
    * *(PM Note: This is the Schema hard-coded in the Dify Prompt. You can download and import this dataset from [GitHub - datacharmer/test_db](https://github.com/datacharmer/test_db).)*

2.  **Database HTTP API Interface:**
    * You need a **public** HTTP API endpoint (e.g., built with Python Flask or Node.js Express).
    * Dify will `POST` the generated SQL query to this API.
    * Your API must accept JSON in the format `{"sql_query": "SELECT..."}`, execute it, and return the query results in JSON format.

---

## 🚀 如何使用

1.  **Set LLM API Keys:**
    * This workflow relies on `langgenius/deepseek` and `langgenius/siliconflow` providers (or other LLM providers).
    * Ensure you have valid API keys set up in Dify's "Credentials" for DeepSeek (for SQL generation) and SiliconFlow (for Kimi analysis) or other LLMs.

2.  **[CORE] Configure Dify HTTP Node:**
    * In the Dify canvas, open the "HTTP Request" node.
    * **URL:** **Replace** the default `http://sql_api:35003/execute_query` with the URL of your own database API endpoint.
    * **Headers:** Configure `Authorization` (e.g., `X-API-Key`) as required by your API.

3.  **Run the Workflow:**
    * In the "Start" node's `user_request` variable, enter your natural language question (e.g., "How many employees are currently in the Engineering department?" or "Who are the top 10 highest-paid employees?").
    * Run the workflow and check the "End" node for the complete analysis report.

## 🛠️ 工作流节点 (Optional)

* **Start Node:** Receives the user's natural language question `user_request`.
* **LLM 1 (SQL Expert):** (Uses `deepseek-coder`) Converts the user question into a MySQL query. The Prompt is hard-coded with the `employees` sample database Schema.
* **HTTP Request Node (User Configured):** Sends the generated SQL query (from LLM 1) to your own database API endpoint.
* **LLM 2 (Data Analyst):** (Uses `Kimi-K2-Instruct`) Receives the JSON data from the HTTP node and the user's original question, summarizing it into a Markdown report and generating an ECharts chart.
* **End Node:** Outputs the final analysis report (including Markdown table and ECharts JSON).

## 📸 运行截图 (Highly Recommended)

### 工作流图
![Workflow Graph](screenshot-workflow.png)

### 运行示例
![Example Run](screenshot-run.png)
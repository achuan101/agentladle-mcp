# 📈 AgentLadle MCP - Financial Reports

*Read this in other languages: [English](README.md) | [简体中文](README_zh-CN.md)*

![AgentLadle Banner](https://agentladle.com/vite.webp)

**AgentLadle** is a specialized Model Context Protocol (MCP) server designed for AI developers and platforms.

By integrating this server, your AI assistants (like Claude) gain the superpower to instantly search, extract, and comprehend the **Annual Financial Reports (2023-2025)** of all listed companies in the **Chinese A-share market** (Shanghai and Shenzhen exchanges).

---

## ✨ Features

- 🔍 **Full-Text Financial Search (`financialKeywordSearch`)**: Pinpoint specific keywords and paragraphs within annual reports across the entire A-share market.
- 📑 **Page Extraction (`getFinancialReportPages`)**: Extract exact, unadulterated pages from any company's annual report for deep reading and context building.
- 📊 **Statements Locator (`getFinancialStatementsStartPages`)**: Instantly locate the starting pages for the four major consolidated financial statements (Balance Sheet, Income Statement, Cash Flow, Statement of Changes in Equity).
- 📖 **Chapter Directory (`getReportChapters`)**: Fetch the complete, structured table of contents for any financial report.
- 🏢 **Company Information (`searchCompanyInfo`)**: Query basic company information by name or stock code.

---

## 🚀 Get Started

### 1. Get Your API Key
AgentLadle is a cloud-hosted API service. To use this MCP server, you must first obtain an API Key.

> [!IMPORTANT]
> 👉 **[Click here to register on AgentLadle.com and get your API Key to use for free](https://agentladle.com/register)**

### 2. Client Configuration

Since AgentLadle is a cloud-hosted service, you **do not** need to install or run any local servers. We use a **stateless HTTP** implementation.

Add the following configuration to your MCP client (e.g., Claude Desktop, Cursor):

```json
{
  "mcpServers": {
    "agentladle-mcp": {
      "type": "streamableHttp",
      "url": "https://mcp.agentladle.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY_HERE"
      }
    }
  }
}
```

*Don't forget to replace `YOUR_API_KEY_HERE` with the actual key you generated in step 1.*

---

## 🛠️ Usage Example

Once configured, simply open Claude Desktop and try asking:
- **Notes Deep Dive & Attribution**: *"Analyze BYD's 2025 accounts receivable breakdown."* or *"Find the direction of CATL's capital expenditures in 2025."*
- **Benchmarking & Restructuring**: *"Extract Gree's 2025 balance sheet and restructure it into a managerial balance sheet."*
- **Thematic Market Scanning**: *"Which companies mentioned 'Solid-State Batteries' in their 2025 annual reports?"* or *"What is the market-wide progress on the 'Low-Altitude Economy'?"*



*This repository acts as an MCP Connector and configuration guide. The core backend services remain hosted securely on AgentLadle's infrastructure.*

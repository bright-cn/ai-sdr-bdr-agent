<div align="center">
  <a href="https://www.bright.cn/">
    <img src="https://mintlify.s3.us-west-1.amazonaws.com/brightdata/logo/light.svg" width="300" alt="Bright Data 标志">
  </a>

# AI BDR/SDR 智能体系统

通过多智能体智能分析和基于触发事件的个性化，实现实时潜客开发。

<img src="https://img.shields.io/badge/python-3.11+-blue" />
<img src="https://img.shields.io/badge/OpenAI-API-blueviolet" />
<img src="https://img.shields.io/badge/License-MIT-blue" />
</div>

<div align="center">
<img src="https://media.brightdata.com/2025/09/AI-SDR-Agent-demo.gif" alt="AI SDR/BDR 智能体演示">
</div>

---

## 概述

该系统使用 **5 个专业 AI 智能体**：
  1. 公司发现智能体：查找符合你的 ICP 的公司
  2. 触发事件检测智能体：识别购买信号和最佳时机
  3. 联系人研究智能体：提取决策者信息
  4. 消息生成智能体：创建个性化推广消息
  5. 销售管道管理器：为潜在客户评分并与 CRM 集成

[**访问我们博客上的分步指南**](https://www.bright.cn/blog/ai/ai-sdr-agent-with-web-mcp)

---

## 前提条件

- Python 3.11+
- Node.js 和 npm（用于 MCP 服务器）
- API 密钥：
    - [OpenAI API 密钥](https://platform.openai.com/api-keys)
    - 拥有网页 MCP 访问权限的 [Bright Data](https://www.bright.cn/) 账户
    - HubSpot CRM 凭据（可选）

---

## 快速开始

1. **克隆并设置：**

   ```bash
   git clone https://github.com/bright-cn/ai-sdr-bdr-agent.git
   cd ai-sdr-bdr-agent
   pip install -r requirements.txt
   ```

2. **配置 API 密钥：**  
   将 `env.example` 复制到 `.env`，并填写你的凭据：

   ```bash
   cp env.example .env
   ```

   ```
   BRIGHT_DATA_API_TOKEN=your_token_here
   WEB_UNLOCKER_ZONE=your_web_unlocker_zone_name
   BROWSER_ZONE=your_browser_zone_name
   OPENAI_API_KEY=your_key_here
   HUBSPOT_API_KEY=your_hubspot_key_here
   ```

3. **运行应用程序：**

   ```bash
   streamlit run ai_bdr_system.py
   ```

---

## 功能

- 多智能体工作流：并行处理、实时数据、评分和 CRM 集成
- 触发事件智能分析：招聘激增、融资、领导层变动和业务扩张
- 个性化引擎：上下文感知、基于触发事件、多渠道和 A/B 测试
- 导出与集成：CSV、HubSpot 同步、字段映射和批量联系人

---

## 系统架构

    ┌─────────────────────────────────────────────────────────────┐
    │                    Streamlit Frontend                      │
    ├─────────────────────────────────────────────────────────────┤
    │                    CrewAI Orchestration                    │
    ├─────────────────────────────────────────────────────────────┤
    │  Discovery │ Triggers │ Contacts │ Messages │ Pipeline      │
    │   Agent    │  Agent   │  Agent   │  Agent   │ Manager       │
    ├─────────────────────────────────────────────────────────────┤
    │    Bright Data MCP │ OpenAI │ HubSpot API                  │
    └─────────────────────────────────────────────────────────────┘

---

## 配置

### ICP 定位
  - 行业选择（SaaS、金融科技、电商等）
  - 公司规模范围
  - 地理位置定位
  - 自定义条件

### 消息类型
  - 冷邮件营销活动
  - LinkedIn 连接请求
  - 跟进序列
  - 自定义模板

### 潜在客户评分
  - ICP 匹配分数（30%）
  - 触发事件分数（30%）
  - 联系人质量分数（20%）
  - 时机优化（20%）

---

## API 集成

### Bright Data MCP
  - 实时网页爬虫
  - LinkedIn 公司数据
  - 新闻和新闻稿
  - 联系信息

### OpenAI GPT-4
  - 消息个性化
  - 内容生成
  - 触发事件分析
  - 潜在客户资格评估

### HubSpot CRM
  - 创建/更新联系人
  - 潜在客户评分同步
  - 自定义属性
  - 销售管道管理

---

## 故障排除

1. MCP 连接错误

   ```bash
   npm install -g @brightdata/mcp
   ```

2. 缺少依赖项

   ```bash
   pip install -r requirements.txt
   ```

3. API 密钥错误

    - 验证 `.env` 文件中的密钥
    - 检查 API 配额和权限

---

## 性能指标

- 发现的公司：15-25 家
- 触发事件：8-15 个
- 优质联系人：40-60 个
- 回复率：15-25%
- 会议预约率：3-8%

---

## 安全与隐私

- API 密钥存储在环境变量中
- 会话结束后不保留任何数据
- 符合 GDPR 要求的联系人数据处理
- 通过速率限制保护 API

---

## 许可证

本项目仅用于教育和内部演示。

---

## 了解更多

- [Bright Data 的网页 MCP 如何运作](https://docs.brightdata.com/mcp-server/overview)
- [Streamlit 文档](https://docs.streamlit.io/)
- [OpenAI 平台文档](https://platform.openai.com/docs)
- [CrewAI 文档](https://docs.crewai.com/)

---

**准备好提升你的销售开发能力了吗？部署你自己的 AI SDR 智能体，立即将人工推广转变为自动化的高质量销售管道！**

<p align="center">
  <a href="https://www.bright.cn/cp/start" target="_blank" style="text-decoration:none;">
    <img src="https://img.shields.io/badge/Get%20Started-%233D7FFC?style=for-the-badge&logo=rocket&logoColor=white" alt="立即开始" style="height: 48px; border-radius: 8px;">
  </a>
</p>

---

**使用 Bright Data 和 OpenAI 倾情打造 ❤️**

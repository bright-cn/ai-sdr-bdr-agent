<div align="center">
  <a href="https://www.bright.cn/">
    <img src="https://mintlify.s3.us-west-1.amazonaws.com/brightdata/logo/light.svg" width="300" alt="Bright Data 标志">
  </a>

# AI BDR/SDR 智能体系统

多智能体协作的实时拓客，基于触发事件的个性化外联。

<img src="https://img.shields.io/badge/python-3.11+-blue" />
<img src="https://img.shields.io/badge/OpenAI-API-blueviolet" />
<img src="https://img.shields.io/badge/License-MIT-blue" />
</div>

<div align="center">
<img src="https://media.brightdata.com/2025/09/AI-SDR-Agent-demo.gif" alt="AI SDR/BDR Agent 演示">
</div>

---

## 概述

该系统由「5 个专业智能体」组成：
  1. 公司发现智能体 — 寻找符合你 ICP（理想客户画像）的公司
  2. 触发信号检测智能体 — 识别购买信号与最佳触达时机
  3. 联系人研究智能体 — 提取关键决策者信息
  4. 信息生成智能体 — 创建个性化外联内容
  5. 流水线管理器 — 线索评分并与 CRM 集成

[访问我们的博客，阅读分步指南](https://www.bright.cn/blog/ai/ai-sdr-agent-with-web-mcp)

---

## 前置条件

- Python 3.11+
- Node.js 与 npm（用于 MCP 服务器）
- API 密钥：
    - [OpenAI API key](https://platform.openai.com/api-keys)
    - 具有 Web MCP 访问权限的 [Bright Data](https://www.bright.cn/) 账号
    - HubSpot CRM 凭据（可选）

---

## 快速开始

1. 克隆与初始化：

        git clone <repository>
        cd AI_BDR_SDR
        python setup.py

2. 配置 API 密钥：  
   编辑 `.env` 文件并填入你的凭据：

        OPENAI_API_KEY=your_key_here
        BRIGHT_DATA_API_TOKEN=your_token_here
        HUBSPOT_API_KEY=your_hubspot_key_here

3. 测试系统：

        python test_workflow.py

4. 运行应用：

        streamlit run ai_bdr_system.py

---

## 功能

- 多智能体工作流：并行处理、实时数据、评分与 CRM 集成
- 触发情报：招聘激增、融资动态、管理层变动、业务扩张
- 个性化引擎：上下文感知、基于触发的多渠道外联、A/B 测试
- 导出与集成：CSV、HubSpot 同步、字段映射与批量联系人

---

## 系统架构

    ┌─────────────────────────────────────────────────────────────┐
    │                    Streamlit 前端                          │
    ├─────────────────────────────────────────────────────────────┤
    │                    CrewAI 编排                             │
    ├─────────────────────────────────────────────────────────────┤
    │  发现 │  触发 │  联系人 │  信息 │  流水线                   │
    │  Agent│ Agent │ Agent  │ Agent │ Manager                   │
    ├─────────────────────────────────────────────────────────────┤
    │    Bright Data MCP │ OpenAI │ HubSpot API                  │
    └─────────────────────────────────────────────────────────────┘

---

## 配置

### ICP 定向
  - 行业选择（SaaS、FinTech、E-commerce 等）
  - 公司规模区间
  - 地理定向
  - 自定义条件

### 信息类型
  - 冷邮件营销
  - LinkedIn 加好友请求
  - 跟进序列
  - 自定义模板

### 线索评分
  - ICP 匹配度（30%）
  - 触发事件得分（30%）
  - 联系人质量（20%）
  - 时机优化（20%）

---

## API 集成

### Bright Data MCP
  - 实时网页抓取
  - LinkedIn 公司数据
  - 新闻与新闻稿
  - 联系方式信息

### OpenAI GPT-4
  - 信息个性化
  - 文本生成
  - 触发分析
  - 线索资格评估

### HubSpot CRM
  - 联系人创建/更新
  - 线索评分同步
  - 自定义属性
  - 流水线管理

---

## 故障排查

1. MCP 连接错误

        npm install -g @brightdata/mcp

2. 依赖缺失

        pip install -r requirements.txt

3. API 密钥错误

    - 核对 `.env` 文件中的密钥
    - 检查配额与权限

### 验证

        python test_workflow.py

---

## 性能指标

- 发现公司数：15-25
- 触发事件：8-15
- 优质联系人：40-60
- 回复率：15-25%
- 预约会议：3-8%

---

## 安全与隐私

- API 密钥存储于环境变量
- 会话结束后不持久化数据
- 符合 GDPR 的联系人处理
- API 保护的限流机制

---

## 许可证

本项目仅用于教育与内部演示目的。

---

## 了解更多

- [Bright Data Web MCP 的工作原理](https://docs.brightdata.com/mcp-server/overview)
- [Streamlit 文档](https://docs.streamlit.io/)
- [OpenAI 平台文档](https://platform.openai.com/docs)
- [CrewAI 文档](https://docs.crewai.com/)

---

准备好提升你的销售开发效率了吗？部署你的 AI SDR 智能体，即刻把手动外联转化为自动化、可验证的高质量销售流水线！

<p align="center">
  <a href="https://www.bright.cn/cp/start" target="_blank" style="text-decoration:none;">
    <img src="https://img.shields.io/badge/Get%20Started-%233D7FFC?style=for-the-badge&logo=rocket&logoColor=white" alt="Get Started" style="height: 48px; border-radius: 8px;">
  </a>
</p>

---

**由 Bright Data 与 OpenAI 倾情打造 ❤️**

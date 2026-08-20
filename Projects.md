# 🚀 项目经历

这里记录个人项目与真实业务场景中的开发实践，重点展示 **AI Agent、RAG、全栈开发、工程集成与业务落地**。

## 🌏 万旅 WanLv｜智慧景区 AI 数字导游平台

面向智慧景区的 AI 数字导游平台，覆盖景区展示、景点预约、智能问答、数字人讲解、导游地图与路线规划等场景。

### 技术栈

`Vue3` · `Spring Boot` · `MySQL` · `AI Agent` · `RAG` · `WebRTC` · `LiveTalking` · `Dijkstra`

### 核心实现

- 独立推进前端、Spring Boot 后端、Agent、数字人及地图模块开发，完成完整业务闭环。
- 搭建垂直景区 Agent 服务，统一处理 **意图识别、RAG 检索、业务 API 调用与回答生成**。
- 将 Agent 与景区、景点、预约、路线等真实业务接口打通，使模型能够调用平台实时数据完成问答与任务执行。
- 基于景区道路 `GeoJSON` 构建路网，将景点吸附至道路节点，并使用 `Dijkstra` 计算最短路径。
- 打通 `Agent → TTS → LiveTalking → WebRTC` 链路，实现 AI 回答、语音合成与数字人口型驱动。
- 管理端支持景区、景点、地图点位、预约规则等数据配置，并结合游客行为生成日报与用户画像。

### 代码仓库

- 🤖 [wanlv-agent](https://github.com/ddddajie/wanlv-agent) — Agent / RAG 服务
- 🌐 [wanlv-web](https://github.com/ddddajie/wanlv-web) — Web 前端
- ⚙️ [wanlv-back](https://github.com/ddddajie/wanlv-back) — 后端服务
- 📱 [wanlv-android](https://github.com/ddddajie/wanlv-android) — Android 客户端
- 🧑‍💻 [Wanlv-livetalking](https://github.com/ddddajie/Wanlv-livetalking) — 数字人模块

---

## 🌾 链慧通｜数字农权交易平台

基于 Spring Boot、区块链与 AI 构建的农权交易平台，将传统多机构线下交易流程数字化。

### 技术栈

`Spring Boot` · `MySQL` · `FISCO BCOS` · `Python` · `Whisper` · `RAG` · `TTS`

### 核心实现

- 设计交易申请、身份验证、流程审核、证书生成与验真等核心业务接口。
- 对接 `FISCO BCOS`，将交易信息、审核记录及鉴证数据进行链上存证，实现过程可追溯与防篡改。
- 部署 `Whisper + 本地大模型`，实现语音输入、信息结构化提取与 JSON 表单自动填充。
- 搭建 RAG 政策问答并接入离线 TTS，同时实现鉴证书链上验真流程。
- 项目将原约 45 天的传统办理流程缩短至约 7 天。

---

## 🧰 AiPDF / AiIQ｜海外 AI 工具站

独立负责两个海外工具站从技术选型、UI 设计、前后端开发到测试部署的完整流程，并完成多语言适配。

### 技术栈

`HTML` · `CSS` · `JavaScript` · `Node.js` · `Cloudflare Workers` · `D1` · `PDF.js` · `pdf-lib` · `LLM`

### AiPDF

- 基于 `PDF.js`、`pdf-lib` 实现 PDF 合并、拆分及常用文档转换能力。
- 采用 **浏览器本地处理 + 服务端转换** 的分层方案，在隐私、成本与复杂文档兼容性之间做平衡。
- 对复杂 Office 文档使用 LibreOffice / 服务端转换方案，避免只提取纯文本导致格式丢失。

### AiIQ

- 完成 `IQ`、`MBTI`、`Big Five`、`Career`、`Love`、`Mental Age` 六类测试。
- 使用 JSON 配置题库与统一评分引擎，实现答题、计分、多维结果分析和报告生成。
- 接入大模型，根据测评结果动态生成个性化分析，并根据当前页面语言返回对应语言内容。
- 完成登录注册、用户中心、管理员后台、基础埋点，以及订阅、权限、订单和 Webhook 架构设计。

---

## 🤖 Medical Tourism｜海外来华就医 AI Agent

面向来华就医场景的医疗业务 Agent 与内部 RAG 系统。

### 技术栈

`Python` · `FastAPI` · `LangChain` · `MySQL` · `RAG`

### 核心实现

- 基于 `LangChain + FastAPI` 搭建 Agent，根据用户意图动态加载 Prompt、业务知识和工具规则。
- 使用 Markdown 对角色约束、业务知识和工具规则进行分类解耦，并根据问题动态匹配加载。
- 使用 MySQL 管理多轮会话上下文，并根据模型上下文长度进行阶段性压缩，降低长会话 Token 消耗。
- 参与文档清洗、Chunk、向量化与召回流程设计，通过 **文档 ID + Hash** 实现知识库更新与删除一致性。
- 约束知识未命中时模型不直接生成医疗结论，降低无依据回答风险。

---

## 📍 Find GPS Locations｜手机号授权定位平台

面向移动端的定位授权产品，完成从支付到授权、定位和结果回传的完整链路。

### 技术栈

`Node.js` · `Cloudflare Workers` · `JavaScript` · `Webhook` · `RESTful API`

### 核心实现

- 负责前后端全栈开发，完成手机号输入、订单创建、支付、短信授权、浏览器定位及结果展示。
- 对接公司支付中台与 BuziPay，完成订单创建、Checkout 跳转和支付状态处理。
- 设计支付 Webhook 流程，根据支付结果更新订单状态并驱动短信授权、定位等后续业务。
- 实现浏览器授权定位与经纬度回传，并完成 Cloudflare Workers 部署及线上联调。

---

## 🏁 Checkwin｜AI 激励式习惯养成平台

结合挑战任务、每日打卡与 AI 辅助审核的习惯养成产品。

### 技术栈

`Node.js` · `Python` · `FastAPI` · `MySQL` · `LLM` · `Prompt Engineering`

### 核心实现

- 参与挑战模板、每日打卡和挑战状态流转等后端业务开发。
- 搭建 AI 图片审核服务，通过 FastAPI 调用大模型，并结合挑战信息动态生成审核 Prompt。
- 实现 `AI 审核 → 异常人工复核 → 状态更新` 的审核流程。
- 参与 AI 教练与动态用户画像设计，根据挑战目标、长期行为和近期状态生成个性化提醒与计划建议。

---

[← 返回个人主页](./README.md)

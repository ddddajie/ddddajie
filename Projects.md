# 🚀 项目经历

这里记录个人项目与真实业务场景中的开发实践，重点展示 **AI Agent、RAG、全栈开发与工程落地**。

## 🌏 万旅 WanLv｜智慧景区 AI 数字导游平台

面向智慧景区的 AI 数字导游平台，覆盖智能问答、景点预约、数字人讲解、地图导览与路线规划等场景。

`Vue3` · `Spring Boot` · `MySQL` · `AI Agent` · `RAG` · `WebRTC` · `LiveTalking` · `Dijkstra`

- 搭建垂直景区 Agent，连接知识库、业务 API、地图与数字人服务。
- 基于景区道路 GeoJSON + Dijkstra 实现专属路线规划。
- 打通 `Agent → TTS → LiveTalking → WebRTC` 数字人讲解链路。

### 代码仓库

- 🤖 [wanlv-agent](https://github.com/ddddajie/wanlv-agent)
- 🌐 [wanlv-web](https://github.com/ddddajie/wanlv-web)
- ⚙️ [wanlv-back](https://github.com/ddddajie/wanlv-back)
- 📱 [wanlv-android](https://github.com/ddddajie/wanlv-android)
- 🧑‍💻 [Wanlv-livetalking](https://github.com/ddddajie/Wanlv-livetalking)

---

## 🌾 链慧通｜数字农权交易平台

基于 Spring Boot、区块链与 AI 构建的农权交易平台，用于交易流程数字化、链上存证与智能辅助办理。

`Spring Boot` · `MySQL` · `FISCO BCOS` · `Python` · `Whisper` · `RAG` · `TTS`

- 实现交易申请、审核、证书生成与验真等核心业务。
- 对接 FISCO BCOS 完成交易与鉴证数据链上存证。
- 接入 Whisper、本地大模型、RAG 与 TTS，支持语音填表与政策问答。

---

## 🧰 AiPDF / AiIQ｜海外 AI 工具站

独立负责两个海外工具站的技术选型、UI、前后端开发、测试部署与多语言适配。

`HTML` · `CSS` · `JavaScript` · `Node.js` · `Cloudflare Workers` · `D1` · `PDF.js` · `pdf-lib` · `LLM`

- **AiPDF**：实现 PDF 合并、拆分及常用文档转换能力。
- **AiIQ**：实现 IQ、MBTI、Big Five、Career、Love、Mental Age 六类测试与统一评分。
- 接入大模型生成个性化测评报告，并完成登录、后台、权限、订单与 Webhook 基础架构。

---

## 🤖 Medical Tourism｜海外来华就医 AI Agent

面向来华就医场景的 AI Agent 与内部 RAG 系统。

`Python` · `FastAPI` · `LangChain` · `MySQL` · `RAG`

- 根据用户意图动态加载 Prompt、业务知识与工具规则。
- 使用 MySQL 管理多轮上下文，并进行阶段性压缩。
- 参与 RAG 文档清洗、向量化、召回及知识库更新一致性设计。

---

## 📍 Find GPS Locations｜手机号授权定位平台

面向移动端的授权定位产品，覆盖支付、短信授权、浏览器定位与结果回传。

`Node.js` · `Cloudflare Workers` · `JavaScript` · `Webhook` · `RESTful API`

- 负责前后端全栈开发与完整业务链路实现。
- 对接支付中台与 BuziPay，并设计支付 Webhook 状态流转。
- 完成 Cloudflare Workers 部署与线上联调。

---

## 🏁 Checkwin｜AI 激励式习惯养成平台

结合挑战任务、每日打卡与 AI 辅助审核的习惯养成产品。

`Node.js` · `Python` · `FastAPI` · `MySQL` · `LLM` · `Prompt Engineering`

- 参与挑战模板、打卡与状态流转等后端开发。
- 搭建 AI 图片审核服务与人工复核流程。
- 参与 AI 教练与动态用户画像设计。

---

[← 返回个人主页](./README.md)

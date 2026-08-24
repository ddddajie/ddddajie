# 🌱 开源经历

# [Dify](https://github.com/langgenius/dify)

### ✅ 已合并

#### [PR #40787 — dep inject for dataset document actions](https://github.com/langgenius/dify/pull/40787)

将 dataset document 接口的请求模型校验迁移到 Dify 现有依赖注入方式，并补充对应测试。

#### [PR #41117 — pass session to workflow comment account accessors](https://github.com/langgenius/dify/pull/41117)

将 workflow comment 的账户访问改为显式传入 SQLAlchemy `Session`，移除隐藏的数据库会话依赖。

### 🚧 进行中

#### [PR #41135 — add vision-aware file upload settings](https://github.com/langgenius/dify/pull/41135)

为 Agent V2 Chat Features 增加 Vision 能力感知，在图片上传场景提示非视觉模型并提供 High / Low 分辨率设置。

#### [Issue #40575 — Add Multi-select / Checkbox Group Input to Start Node User Input](https://github.com/langgenius/dify/issues/40575)

为 Dify Start Node 实现原生 `multi-select` 输入支持，并在 [Graphon PR #259](https://github.com/langgenius/graphon/pull/259) 中补充对应变量类型能力。

### 🤝 协作贡献

#### [PR #40965 — fix dataset re-index after embedding model switch](https://github.com/langgenius/dify/pull/40965)

在 Review 中定位 `RAG_PIPELINE` 场景下 `after_commit` listener 注册顺序问题，并提出被采纳的修复与回归测试方案。

# [Vite](https://github.com/vitejs/vite)

### 🚧 进行中

#### [PR #23343 — inject browser hash into node_modules module scripts](https://github.com/vitejs/vite/pull/23343)

针对 [Issue #9828](https://github.com/vitejs/vite/issues/9828)，修复开发模式下 HTML 直接引用 `node_modules` 模块未注入 `browserHash`、导致同一模块被重复实例化的问题。

# [LangGraph](https://github.com/langchain-ai/langgraph)

### 🚧 进行中

#### [PR #8663 — Replace unnecessary BaseException catches with Exception](https://github.com/langchain-ai/langgraph/pull/8663)

针对 [Issue #7900](https://github.com/langchain-ai/langgraph/issues/7900)，收窄 cleanup 与 task callback 路径中过度捕获的 `BaseException`，避免 `KeyboardInterrupt` / `SystemExit` 被静默吞掉。

#### [Issue #6896 — checkpoint-sqlite: make TTL pruning deterministic at boundary](https://github.com/langchain-ai/langgraph/issues/6896)

修复 SQLite TTL 清理在亚秒边界上的时间精度不一致问题，并补充同步/异步回归测试。

---

[← 返回个人主页](./README.md)

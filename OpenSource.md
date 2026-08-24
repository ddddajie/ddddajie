# 🌱 开源经历

## LangGraph

#### [PR #8663 — Replace unnecessary BaseException catches with Exception](https://github.com/langchain-ai/langgraph/pull/8663)

针对 [Issue #7900](https://github.com/langchain-ai/langgraph/issues/7900)，收窄 cleanup 与 task callback 路径中过度捕获的 `BaseException`，避免 `KeyboardInterrupt` / `SystemExit` 被静默吞掉。

## Dify

#### [PR #40787 — dep inject for dataset document actions](https://github.com/langgenius/dify/pull/40787)

将 dataset document 接口的请求模型校验迁移到 Dify 现有依赖注入方式，并补充对应测试。

#### [PR #41117 — pass session to workflow comment account accessors](https://github.com/langgenius/dify/pull/41117)

针对 [Issue #40372](https://github.com/langgenius/dify/issues/40372)，将 workflow comment 数据库访问改为显式传入 SQLAlchemy `Session`，明确数据库依赖与事务边界。

#### [Issue #40575 — Add Multi-select / Checkbox Group Input to Start Node User Input](https://github.com/langgenius/dify/issues/40575)

为 Dify Start Node 实现原生 `multi-select` 输入支持，并在 [Graphon PR #259](https://github.com/langgenius/graphon/pull/259) 中补充对应变量类型能力。

### 🤝 协作贡献

#### [PR #40965 — fix dataset re-index after embedding model switch](https://github.com/langgenius/dify/pull/40965)

在 Review 中定位 `RAG_PIPELINE` 场景下 `after_commit` listener 注册顺序问题，并提出被采纳的修复与回归测试方案。

---

[← 返回个人主页](./README.md)

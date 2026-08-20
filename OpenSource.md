# 🌱 开源经历

## Dify

参与 [langgenius/dify](https://github.com/langgenius/dify) 的后端开源贡献，主要关注依赖注入、数据库 Session 边界与业务逻辑问题分析。

### ✅ 已合并

#### [PR #40787 — dep inject for dataset document actions](https://github.com/langgenius/dify/pull/40787)

将部分 dataset document 接口的请求模型校验迁移到 Dify 现有的依赖注入方式，并同步更新相关测试。

**状态：已合并**

### 🚧 进行中

#### [PR #40873 — pass session to workflow comment account accessors](https://github.com/langgenius/dify/pull/40873)

将 workflow comment 相关数据库访问从隐式 `db.session` 调整为显式传入 SQLAlchemy `Session`，使依赖边界更清晰。

**状态：Open**

### 🤝 协作贡献

#### [PR #40965 — fix dataset re-index after embedding model switch](https://github.com/langgenius/dify/pull/40965)

在 Review 中发现 `RAG_PIPELINE` 场景下 `after_commit` listener 注册顺序存在边界问题，并提出将 listener 提前注册、补充回归测试的修复思路。PR 作者确认问题成立并采纳方案，随后完成对应代码与测试调整。

**状态：Open · 建议已采纳**

---

[← 返回个人主页](./README.md)

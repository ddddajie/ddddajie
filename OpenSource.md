# 🌱 开源经历

这里记录我参与开源项目时的 Issue 分析、代码修改、Pull Request 与后续贡献。

## Dify

参与 [langgenius/dify](https://github.com/langgenius/dify) 的后端代码贡献，目前主要关注依赖注入、数据库 Session 边界、接口重构与测试覆盖。

### ✅ 已合并

#### [PR #40787 — chore: dep inject for model in dataset document actions](https://github.com/langgenius/dify/pull/40787)

- 将部分 dataset document 接口中的 `model_validate(...)` 内联校验迁移到 Dify 现有的 `@model_validate` 依赖注入方式。
- 更新受影响的单元测试，使测试适配新的请求模型注入流程。
- 保持业务逻辑、数据库结构与原有行为不变，控制修改范围。

### 🚧 进行中

#### [PR #40873 — refactor: pass session to workflow comment account accessors](https://github.com/langgenius/dify/pull/40873)

- 将 workflow comment 相关 account accessor 改为显式接收调用方传入的 SQLAlchemy `Session`。
- 减少 model 层对全局 `db.session` 的隐式依赖，使数据库依赖边界更清晰。
- 保留原有 account cache、参与者去重与事务语义，并同步调整 model、service、controller 与相关测试。

## 📌 后续记录方式

后续每次开源贡献会按以下信息持续补充：

- Issue / PR 编号
- 当前状态（进行中 / 已合并）
- 问题背景与修改内容
- 测试与验证结果
- 最终合并结果

---

[← 返回个人主页](./README.md)

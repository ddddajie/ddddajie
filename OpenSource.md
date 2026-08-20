# 🌱 开源经历

这里记录我参与开源项目时的 Issue 分析、代码修改、Pull Request 与后续贡献。

## Dify

参与 [langgenius/dify](https://github.com/langgenius/dify) 的后端代码贡献，目前主要关注 **依赖注入、数据库 Session 边界、接口重构与测试覆盖**。

### ✅ 已合并

#### [PR #40787 — chore: dep inject for model in dataset document actions](https://github.com/langgenius/dify/pull/40787)

**目标**：将部分 dataset document 接口中的请求模型校验，从内联 `model_validate(...)` 调用迁移到 Dify 现有的 `@model_validate` 依赖注入方式。

**主要修改**

- 调整 `DocumentRetryApi.post`、`DocumentRenameApi.post`、`DocumentGenerateSummaryApi.post` 的请求模型注入方式。
- 更新受影响的单元测试，使测试适配新的 validated request model 注入流程。
- 保持原有业务逻辑、数据库交互和接口行为不变，控制修改范围。

**验证结果**

- dataset document 相关单测：**71 passed**
- wraps 相关测试：通过
- Ruff lint / format：通过

**状态**：已合并至 Dify 主仓库。

---

### 🚧 进行中

#### [PR #40873 — refactor: pass session to workflow comment account accessors](https://github.com/langgenius/dify/pull/40873)

**目标**：将 workflow comment 相关 account accessor 从隐式访问全局 `db.session`，改为显式接收调用方传入的 SQLAlchemy `Session`。

**主要修改**

- 为 `WorkflowComment`、`WorkflowCommentReply`、`WorkflowCommentMention` 的 account accessor 增加显式 `Session` 参数。
- 在 `WorkflowComment.participants` 中继续传递同一个 Session，同时保留 account cache 与参与者去重逻辑。
- 在 controller 边界构建响应模型，使依赖 Session 的值在明确位置完成解析。
- 同步调整 model、service、controller 相关调用点与测试。

**设计目标**

- 减少 model 层对全局数据库 Session 的隐式依赖。
- 保持原有缓存、参与者去重、响应结构和事务语义不变。

**当前验证**

- Ruff lint / format：通过
- `git diff --check`：通过
- Targeted pytest / full type check：受本地依赖环境限制，尚未完整执行

**状态**：Open，等待后续 review / CI 结果。

---

## 📌 记录规则

后续每次开源贡献统一记录：

- Issue / PR 编号与链接
- 当前状态（进行中 / 已合并 / 已关闭）
- 问题背景与修改目标
- 核心代码变更
- 测试与验证结果
- 最终合并结果

[← 返回个人主页](./README.md)

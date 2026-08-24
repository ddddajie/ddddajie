# 🌱 开源经历

## LangGraph

参与 [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) 的开源贡献，主要关注运行时异常处理、流式执行与回归测试。

### 🚧 进行中

#### [PR #8663 — Replace unnecessary BaseException catches with Exception](https://github.com/langchain-ai/langgraph/pull/8663)

针对 [Issue #7900](https://github.com/langchain-ai/langgraph/issues/7900)，修复 cleanup / task callback 路径中过度捕获 `BaseException` 的问题，将 3 处静默吞掉系统级异常的处理收窄为 `Exception`，使 `KeyboardInterrupt` / `SystemExit` 能够正常传播。

修改范围保持在 4 个文件，并补充 sync / async stream mux 与 `BackgroundExecutor` 的 regression tests；相关目标测试、完整 `test_pregel.py`、Ruff 与 `git diff --check` 均已通过。

**状态：代码完成 · PR 因 LangGraph 外部贡献者需先被分配 Issue 而被 Bot 自动关闭 · 等待 Maintainer assignment 后自动重新开放**

## Dify

参与 [langgenius/dify](https://github.com/langgenius/dify) 的后端开源贡献，主要关注依赖注入、数据库 Session 边界与业务逻辑问题分析。

### ✅ 已合并

#### [PR #40787 — dep inject for dataset document actions](https://github.com/langgenius/dify/pull/40787)

将部分 dataset document 接口的请求模型校验迁移到 Dify 现有的依赖注入方式，并同步更新相关测试。

**状态：已合并**

### 🚧 进行中

#### [PR #41117 — pass session to workflow comment account accessors](https://github.com/langgenius/dify/pull/41117)

针对 [Issue #40372](https://github.com/langgenius/dify/issues/40372)，将 workflow comment 相关数据库访问从隐式 `db.session` 调整为显式传入 SQLAlchemy `Session`，并同步适配 controller 与回归测试，使数据库依赖和事务边界更清晰。

该 PR 为 #40873 的更新版本：在原 PR 因与最新 `main` 冲突被关闭后，重新 rebase 到最新主分支、解决测试夹具冲突，并将最终修改范围收敛为 4 个核心文件。

**状态：Open · 无合并冲突 · Review 中**

#### [Issue #40575 — Add Multi-select / Checkbox Group Input to Start Node User Input](https://github.com/langgenius/dify/issues/40575)

为 Dify Start Node 的 User Input 设计并完成原生 `multi-select` 支持，使预定义选项可以作为原生 `string[] / array[string]` 传递给下游节点，并覆盖 required 空数组校验、选项合法性、重复值校验与顺序保持等行为。

前置依赖已在 [Graphon PR #259 — feat: add multi-select input variable type](https://github.com/langgenius/graphon/pull/259) 中实现，新增 `VariableEntityType.MULTI_SELECT` 并复用现有 `ARRAY_STRING` runtime 类型。Dify 侧已完成 backend validation / typing、Start Node 配置、Chat / Embedded Chat / Run Once 等 runtime 支持及对应回归测试，目前代码已推送至个人 fork。

**状态：Dify 实现完成 · Graphon PR #259 Open · 等待前置依赖合并 / 发布后提交 Dify upstream PR**

### 🤝 协作贡献

#### [PR #40965 — fix dataset re-index after embedding model switch](https://github.com/langgenius/dify/pull/40965)

在 Review 中发现 `RAG_PIPELINE` 场景下 `after_commit` listener 注册顺序存在边界问题，并提出将 listener 提前注册、补充回归测试的修复思路。PR 作者确认问题成立并采纳方案，随后完成对应代码与测试调整。

**状态：Open · 建议已采纳**

---

[← 返回个人主页](./README.md)

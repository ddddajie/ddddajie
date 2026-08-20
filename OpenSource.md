# 🌱 开源经历

这里记录我参与开源项目时的 Issue、Pull Request 与代码贡献。

## Dify

参与 [langgenius/dify](https://github.com/langgenius/dify) 的后端代码贡献，主要关注依赖注入、数据库 Session 边界与接口重构。

### ✅ 已合并

#### [PR #40787 — dep inject for dataset document actions](https://github.com/langgenius/dify/pull/40787)

将部分 dataset document 接口的请求模型校验迁移到 Dify 现有的依赖注入方式，并同步更新相关测试。

**状态：已合并**

### 🚧 进行中

#### [PR #40873 — pass session to workflow comment account accessors](https://github.com/langgenius/dify/pull/40873)

将 workflow comment 相关数据库访问从隐式 `db.session` 调整为显式传入 SQLAlchemy `Session`，使依赖边界更清晰。

**状态：Open**

---

[← 返回个人主页](./README.md)

# AI Agent & Developer Guardrails (开发规范法则)

## 核心开发铁律

1. **原子化提交 (Atomic Commit)**[cite: 1, 3]
   - 每一个独立的功能模块、API 接口实现或 Bug 修复，必须单独创建一个对应的 Git Commit[cite: 1, 3]。
   - 严禁将多个不相干的功能块混合在一个 Commit 中提交[cite: 1, 3]。

2. **测试驱动与质量红线 (TDD & Quality Gate)**[cite: 1, 3]
   - 在交付任何代码或创建 Git Commit 前，必须编写对应的 JUnit 单元测试[cite: 1, 3]。
   - 必须运行测试套件，确保 VS Code 中所有测试用例 **100% 绿色通过 (PASS)** 之后，才允许提交代码[cite: 1, 3]。

3. **架构分层规范**
   - 严格遵循 `Controller` -> `Service` -> `Repository` 三层架构设计。
   - 业务逻辑写入 Service 层，Controller 层只负责接收 HTTP 请求与返回 JSON 响应。
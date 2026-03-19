# Project Charter
# 项目章程

## Document Role
## 文档角色

This document stores the durable scope, constraints, non-goals, and architectural principles for the framework effort.<br>
本文件存放该框架工作的长期范围、约束、非目标和架构原则。

Change this document only when a rule should remain valid across multiple iterations.<br>
只有当某条规则需要跨多个迭代持续有效时，才修改本文件。

## Mission
## 使命

Build a maintainable desktop framework foundation that can evolve beyond the current sample application.<br>
构建一个可维护的桌面框架基础，使其能够超越当前示例应用持续演进。

Use the current Tauri-based app as a practical starting point, not as the permanent limit of the architecture.<br>
将当前基于 Tauri 的应用视为务实的起点，而不是架构的永久边界。

## In Scope
## 范围内事项

Framework structure, module boundaries, and application composition are in scope.<br>
框架结构、模块边界和应用组装方式属于范围内事项。

Desktop shell concerns, frontend-backend contracts, and native capability exposure are in scope.<br>
桌面壳层问题、前后端契约以及原生能力暴露方式属于范围内事项。

Developer workflow, build validation, test expectations, and governance documentation are in scope.<br>
开发工作流、构建校验、测试期望和治理文档属于范围内事项。

## Out of Scope
## 非目标

One-off experiments that bypass documented decisions are out of scope for the mainline architecture.<br>
绕过已记录决策的一次性试验，不属于主线架构的目标范围。

Platform-specific shortcuts without an abstraction plan are out of scope.<br>
没有抽象方案的平台特定捷径不属于目标范围。

Large infrastructure commitments outside the desktop framework problem are out of scope unless explicitly adopted later.<br>
除非后续被明确纳入，否则超出桌面框架问题的大型基础设施承诺不属于目标范围。

## Long-Lived Constraints
## 长期约束

Prefer explicit module boundaries over implicit coupling.<br>
优先选择显式模块边界，而不是隐式耦合。

Keep business logic testable outside Tauri command handlers whenever practical.<br>
在可行情况下，应使业务逻辑能够脱离 Tauri 命令处理器进行测试。

Expose only the minimum required native capabilities and keep permission surfaces small.<br>
只暴露最小必要的原生能力，并保持权限面尽可能小。

Assume Windows and macOS are the primary target platforms unless a later decision expands support.<br>
除非后续决策扩大支持范围，否则默认 Windows 和 macOS 是主要目标平台。

Avoid adding dependencies that create long-term maintenance cost without a clear justification.<br>
避免引入缺乏明确理由且会带来长期维护成本的依赖。

## Architecture Principles
## 架构原则

Separate application shell concerns from domain logic.<br>
将应用壳层关注点与领域逻辑分离。

Prefer typed contracts between the frontend and Rust command layer.<br>
优先在前端与 Rust 命令层之间建立类型化契约。

Keep I/O boundaries explicit, especially for filesystem, network, and OS integration.<br>
保持 I/O 边界显式，尤其是文件系统、网络和操作系统集成边界。

Use ADRs for decisions that are expensive to reverse or easy to forget.<br>
对难以回退或容易被遗忘的决策使用 ADR 进行记录。

Optimize for incremental evolution instead of large irreversible rewrites.<br>
优先支持渐进演进，而不是进行大规模且不可逆的重写。

## Quality Bar
## 质量标准

New behavior should have validation proportional to its risk and surface area.<br>
新行为应具有与其风险和影响范围相匹配的验证手段。

Affected code should pass the relevant build, type-check, and test steps before it is treated as complete.<br>
受影响代码在被视为完成前，应通过相关的构建、类型检查和测试步骤。

Public behavior changes should be reflected in the active plan, user-facing docs, or both as appropriate.<br>
公开行为变化应视情况同步更新到当前计划、用户文档或两者之中。

Temporary shortcuts must be labeled clearly and should have an explicit removal condition.<br>
临时性捷径必须清晰标注，并应具备明确的移除条件。

## Dependency Policy
## 依赖准入规则

Prefer the standard library and the existing project stack before adding a new package or crate.<br>
在新增 package 或 crate 之前，优先使用标准库和现有项目技术栈。

Every significant dependency should have a clear purpose, acceptable maintenance posture, and reasonable cross-platform fit.<br>
每个重要依赖都应具备明确用途、可接受的维护状态和合理的跨平台适配性。

Record notable dependency additions in the active plan or an ADR when the choice affects long-term architecture.<br>
当某个依赖选择会影响长期架构时，应将其记录在当前计划或 ADR 中。

## Change Control
## 变更控制

Put iteration-specific work breakdowns in `docs/plans/_active.md`.<br>
将迭代级工作拆解放在 `docs/plans/_active.md` 中。

Promote durable rules from the active plan into this charter.<br>
将当前计划中的长期规则提升到本 charter 中。

Promote durable technical decisions from the active plan into `docs/adr/`.<br>
将当前计划中的长期技术决策提升到 `docs/adr/` 中。

Archive completed plans only after durable content has been extracted.<br>
只有在长期内容被抽取之后，才归档已完成计划。

## Tauri Default Assumptions
## Tauri 默认假设

The default desktop stack is Tauri 2 with a Rust backend and a React plus TypeScript frontend.<br>
默认桌面技术栈为 Tauri 2，后端使用 Rust，前端使用 React 加 TypeScript。

The default frontend development flow uses Vite for local development and static assets for desktop bundling.<br>
默认前端开发流程使用 Vite 进行本地开发，并使用静态资源进行桌面打包。

Tauri commands should expose narrow interfaces and avoid becoming a catch-all service layer.<br>
Tauri 命令应暴露窄接口，避免演变成无边界的通用服务层。

Capability declarations should follow least-privilege principles.<br>
能力声明应遵循最小权限原则。

The current repository uses `TestTauri` as the sample application location, but future framework extraction should not be blocked by that initial layout.<br>
当前仓库使用 `TestTauri` 作为示例应用位置，但未来框架抽取工作不应被这一初始布局所限制。

# Active Plan
# 当前计划

## Document Role
## 文档角色

This file is the only active implementation plan for the repository at any given time.<br>
本文件是在任意时刻仓库中唯一生效的实施计划。

Replace this file in place when the active milestone changes.<br>
当当前里程碑发生变化时，应原位替换本文件内容。

Move durable rules into the charter and durable technical decisions into ADRs before archiving this plan.<br>
在归档本计划前，应先将长期规则移入 charter，将长期技术决策移入 ADR。

## Current Objective
## 当前目标

Establish a governed framework baseline around the current Tauri sample so future iterations can build on stable rules and structure.<br>
围绕当前 Tauri 示例建立受治理的框架基线，使后续迭代能够建立在稳定规则和结构之上。

## Phase Status
## 阶段状态

Current phase: foundation setup.<br>
当前阶段：基础搭建。

Current repository baseline: the runnable sample app is located in `TestTauri`.<br>
当前仓库基线：可运行的示例应用位于 `TestTauri`。

## Assumptions
## 前提假设

The repository root is the governance boundary for the current framework effort.<br>
仓库根目录是当前框架工作的治理边界。

The Tauri app remains the executable reference implementation until a broader package structure is introduced.<br>
在引入更广泛的包结构之前，Tauri 应用将继续作为可执行参考实现。

Desktop-first development is the default assumption for the near term.<br>
桌面优先开发是近期默认假设。

## Workstreams
## 工作流分解

Governance: keep project rules, scope, and archive policy explicit and easy to discover.<br>
治理：保持项目规则、范围和归档策略显式且易于发现。

Architecture baseline: define stable seams between frontend UI, Rust commands, and future domain modules.<br>
架构基线：定义前端 UI、Rust 命令层和未来领域模块之间的稳定边界。

Tooling baseline: keep build, type-check, and platform assumptions visible enough for future automation.<br>
工具基线：让构建、类型检查和平台假设足够清晰，以便后续自动化接入。

Decision capture: move any long-lived technical choices into ADRs as they become concrete.<br>
决策沉淀：当长期技术选择变得明确时，将其沉淀到 ADR 中。

## Decisions Currently Locked
## 当前已锁定决策

There is exactly one active plan at a time.<br>
任意时刻只保留一份当前计划。

Archived plans are historical references and are not active instructions.<br>
归档计划是历史参考资料，不是当前指令。

Governance documents use stacked bilingual lines instead of side-by-side tables.<br>
治理文档使用上下堆叠的双语行格式，而不是左右并排表格。

## Risks
## 风险

Template code from the sample app may leak into the framework without deliberate abstraction.<br>
示例应用中的模板代码可能会在缺乏刻意抽象的情况下渗入框架。

Native capability growth can become hard to control if permissions are expanded ad hoc.<br>
如果权限按临时需求扩张，原生能力边界会变得难以控制。

Rules may drift across sessions if durable instructions are left only in chat instead of project documents.<br>
如果长期指令只留在聊天中而不写入项目文档，不同会话之间的规则会发生漂移。

## Acceptance Criteria
## 验收标准

Project governance documents exist at the repository root and define read order, precedence, and document roles.<br>
仓库根目录下已存在项目治理文档，并定义了读取顺序、优先级和文档职责。

The current implementation window is described here without mixing durable charter content into iteration details.<br>
当前实施窗口已在此文件中描述，且未将长期 charter 内容与迭代细节混杂。

The team can decide whether a new rule belongs in the charter, the active plan, or an ADR without ambiguity.<br>
团队能够明确判断一条新规则应进入 charter、当前计划还是 ADR。

## Exit Criteria
## 退出条件

This plan can be replaced once the next concrete milestone is defined and durable learnings from this phase have been extracted.<br>
当下一个具体里程碑被定义且本阶段的长期经验已被抽取后，本计划即可被替换。

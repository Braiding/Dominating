# Archive Policy
# 归档策略

## Purpose
## 目的

This directory stores completed plans that still have historical value.<br>
本目录用于存放仍具有历史价值的已完成计划。

Archived plans do not enter the default instruction chain for normal implementation work.<br>
归档计划不会进入日常实施工作的默认指令链路。

## What To Preserve In Full
## 需要完整保留的内容

Preserve milestone plans that changed architecture, delivery strategy, or repository shape in a meaningful way.<br>
对于显著改变架构、交付策略或仓库形态的里程碑计划，应完整保留。

Preserve plans that contain important decision history, tradeoffs, or rejected alternatives that may matter later.<br>
对于包含重要决策历史、权衡过程或未来可能仍有价值的备选方案的计划，应完整保留。

## What To Summarize Or Drop
## 需要摘要保留或丢弃的内容

Summarize transient task breakdowns once their work is complete and their details no longer affect future implementation.<br>
当临时任务拆解已执行完毕且其细节不再影响未来实施时，应仅保留摘要。

Drop duplicated drafts or short-lived planning notes that were fully superseded before implementation.<br>
对于在实施前就已被完全覆盖的重复草稿或短期计划笔记，应予以删除。

## Naming Convention
## 命名规则

Use `YYYY-MM-topic.md` for archived plan files.<br>
归档计划文件使用 `YYYY-MM-topic.md` 命名格式。

Use concise topic names that describe the milestone rather than the author or meeting.<br>
主题名称应简洁描述里程碑，而不是作者或会议名称。

## Pre-Archive Checklist
## 归档前检查项

Move durable scope or constraint changes into `docs/governance/charter.md`.<br>
将长期有效的范围或约束变更移入 `docs/governance/charter.md`。

Move durable technical decisions into `docs/adr/`.<br>
将长期有效的技术决策移入 `docs/adr/`。

Confirm that `docs/plans/_active.md` has already been updated for the next current milestone or intentionally left as the active source of truth.<br>
确认 `docs/plans/_active.md` 已为下一个当前里程碑更新，或被有意保留为当前事实来源。

## Read Behavior
## 阅读行为

Read archived plans only when you need background on why a decision or milestone happened.<br>
只有在需要了解某项决策或里程碑发生原因时，才阅读归档计划。

Do not treat an archived plan as active guidance unless a newer document explicitly points back to it.<br>
除非较新的文档明确回指，否则不要将归档计划视为当前指导文件。

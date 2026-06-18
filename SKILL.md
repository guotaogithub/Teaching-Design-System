---
name: teaching-design-system
description: 中职/计算机类教师招聘 10 分钟无生试讲工作流。Use when Codex needs to create a lesson design, write a teaching script, review an existing script, revise a script, or turn textbook/course material into a standard trial-lecture artifact based on the internalized V2.0 teaching-script standard.
---

# Teaching Design System

本 Skill 用于生成、审查和修改中职/计算机类教师招聘复试的 10 分钟无生试讲内容。它的目标不是机械完成教学流程，而是呈现一堂真实、自然、有教学逻辑的课堂。

## 基准与保留

`Prompts/逐字稿生成标准V2.0.md` 是本项目的原始基准文档，必须保留，用于追溯、对照和后续校验。日常执行时，不要反复整篇读取它；本 Skill 已将其核心规则拆分并内化到 `references/` 下的工作文件中。

只有在以下情况读取原始 V2.0 文档：

- 用户要求核对 Skill 是否偏离原始标准。
- 用户要求更新、审计或重构标准本身。
- 生成结果与 `references/` 规则冲突，需要回到母版确认。

## 核心总规

所有教学设计、导入、提问、互动、评价、板书和逐字稿表达，都必须服务于知识建构和教学目标达成，避免为了流程而流程。

坚持以下底线：

- 试讲总时长控制在 8 分 30 秒到 9 分 30 秒，教师实际说话字数控制在 950 到 1100 字。
- 课堂结构采用：导入新课、 新课讲授、 巩固练习、 课堂小结、 布置作业。
- 一节课聚焦最适合本次试讲展开的重点知识，数量由材料强度、逻辑连贯性、试讲容量、逐字稿字数和试讲者发挥流畅度共同决定；简单内容轻量串联，复杂内容合理留白。
- 互动服务于知识建构；学生回答后采用“请坐、复述提炼、自然推进”的处理方式。
- 教师语言口语化、评价具体、过渡自然，避免模板化夸奖。
- 板书随讲随写，只写关键词。
- 思政自然融入课堂，不喧宾夺主。

## 策略文件映射

当需要读取教学策略时，必须使用以下精确文件名。不要根据环节名称自行推测文件名。

- 导入环节：`Strategy-Library/Introduction_Strategy.md`
- 提问设计：`Strategy-Library/Questioning_Strategy.md`
- 互动设计：`Strategy-Library/Interaction_Strategy.md`
- 知识讲解：`Strategy-Library/Explanation_Strategy.md`
- 环节过渡：`Strategy-Library/Transition_Strategy.md`
- 板书设计：`Strategy-Library/Blackboard_Strategy.md`
- 巩固练习：`Strategy-Library/Practice_Strategy.md`
- 学生评价：`Strategy-Library/Evaluation_Strategy.md`
- 课堂收束：`Strategy-Library/Closing_Strategy.md`

## 功能路由

根据用户请求选择最小必要流程，不要一次性读取所有参考文件或策略库。

### 1. 创建新课程内容

当用户提供课题、教材片段、知识点或课程材料，并希望生成完整试讲内容时：

1. 读取 `references/standard-core.md`。
2. 读取 `references/content-selection.md`，对材料进行主线提炼、重点选择和留白判断。
3. 读取 `references/lesson-design.md`，生成教学设计骨架。
4. 根据课题性质，从 `Strategy-Library/` 中按需读取相关策略。先给出选择理由，再读取文件；通常选择 3 到 5 个，材料简单时可少于 3 个，确有必要时可多于 5 个。
5. 若用户需要逐字稿，继续读取 `references/script-writing.md`，基于已完成的教学设计扩写逐字稿。
6. 用 `references/script-review.md` 的自检规则检查结果；如有明显不合格项，自动修订一次后再输出。

### 2. 只生成教学设计

读取：

- `references/standard-core.md`
- `references/content-selection.md`
- `references/lesson-design.md`
- 必要的 `Strategy-Library/` 策略文件

输出五环节教学设计骨架，并说明内容取舍依据。

### 3. 只生成逐字稿

当用户已有教学设计、教案骨架或明确课堂流程时，读取：

- `references/standard-core.md`
- `references/script-writing.md`

必要时补读 `references/lesson-design.md` 来修补骨架缺口。输出逐字稿、纯讲话字数统计和 Checklist。

### 4. Review 现成逐字稿

当用户提供已有逐字稿并要求检查、评价、诊断或 review 时，读取：

- `references/standard-core.md`
- `references/script-review.md`

按严重程度输出问题，优先指出会影响考场表现的结构、逻辑、互动、语言、字数和排版问题。

### 5. 修改现成逐字稿

当用户要求润色、优化、压缩、扩写或重写已有逐字稿时：

1. 先按 `references/script-review.md` 做诊断。
2. 再读 `references/script-revision.md` 执行修改。
3. 保留原课题意图和可用亮点，只修正不符合标准的结构、语言、互动、板书、思政、字数和收束问题。

## 渐进披露规则

- `references/standard-core.md` 是常用基础规则，几乎所有任务都应读取。
- 只读取当前功能需要的 reference 文件。
- 策略库是候选组件库，不是必读全集。只读取与当前课题和环节相关的策略。
- 日常生成优先使用 `references/` 工作流；`Prompts/` 仅保留原始 V2.0 母版用于追溯、对照和审计。

## 输出要求

生成逐字稿时，最后必须附：

- 纯讲话字数统计。
- 基于标准的 Checklist。
- 若有不满足项，先修订再给最终稿；无法完全满足时，明确说明原因。

# Teaching Design System (计算机网络试讲教学设计系统)

本项目致力于为**计算机网络教师招聘面试（10分钟无生试讲）**提供一套标准化、可复用、并可由大语言模型（AI）自动化生成高质量教案与逐字稿的解决方案。

## 🎯 核心理念 (Core Philosophy)
拒绝大而全的传统教育学理论，一切为了**考场拿分**与**落地实战**。
坚持**“标准内核化 → 渐进披露 → 教学设计骨架化 → 逐字稿标准化 → Review/修订闭环”**的工作流，用 AI 降低撰写试讲稿的门槛，同时利用严格的标准约束消除 AI 生成的“假大空”问题。

## 🚀 北极星工作流 (North Star Workflow)
1. **Standard Core (标准内核)**：`Prompts/逐字稿生成标准V2.0.md` 保留为原始基准文档；其核心规则已拆入 `references/`，作为 Skill 的日常执行内核。
2. **Progressive Disclosure (渐进披露)**：根据任务只读取必要规则，如内容选取、教学设计、逐字稿撰写、逐字稿 review 或修订。
3. **Strategy Library (教学策略库)**：沉淀适用于 10 分钟试讲的高频互动与讲解策略，作为教案生成的结构化积木。
4. **Lesson Design (教学设计)**：从教材材料中提炼主线，根据内容强度、逻辑连贯和试讲容量判断重点数量，搭建 5 步教学设计骨架。
5. **Teaching Script + Review (逐字稿与审校)**：基于教学设计生成 950-1100 字逐字稿，并按标准自检、review 和修订。

## 📂 目录结构 (Directory Structure)
- `Prompts/`：仅保留原始 V2.0 标准母版，用于追溯、对照和审计。
- `references/`：Skill 的标准内核与任务工作流，按需承载内容选取、教学设计、逐字稿撰写、review 和修订规则。
- `Strategy-Library/`：**核心资产区！** 包含导入、提问、互动、讲解、过渡、板书、练习、评价、总结等 9 大模块的结构化策略卡片。
- `Courses/`：用于存放未来使用引擎生成的优质教案和逐字稿实例（Course Library）。

## 🛠 如何使用 (How to use)
1. **输入课题**：准备好你的试讲题本（教材内容片段）。
2. **内容选取**：按 `references/content-selection.md` 提炼主线，根据材料强度、逐字稿容量和试讲流畅度判断重点数量。
3. **生成教案骨架**：按 `references/lesson-design.md` 和必要策略模块生成五环节教学设计。
4. **生成逐字稿**：按 `references/script-writing.md` 扩写 950-1100 字考场逐字稿。
5. **Review 与修订**：按 `references/script-review.md` 和 `references/script-revision.md` 检查、修改现成逐字稿。

---
name: teaching-design-system
description: 计算机网络教师招聘面试的 10 分钟试讲教案（Lesson Design）与逐字稿（Teaching Script）生成引擎。当用户需要对某一段课本内容进行试讲准备时，必须调用此技能。
---

# Teaching Design System (计算机网络试讲教案与逐字稿生成)

本技能用于帮助备考中高职计算机网络教师招聘面试的用户，根据教材文本，自动切片、组装并生成结构化的“10 分钟无生试讲教案”与极限贴合考场纪律的“纯净版逐字稿”。

为了保证产出质量，本技能采用“两阶段强制工作流”，请**严格按顺序执行**，绝不允许直接跳过教案生成逐字稿。

## 核心原则 (Core Principles)

1. **现实工程与常识优先**：在构建教案与话术逻辑时，严禁盲目顺从教材字面排版顺序。必须引导虚拟学生根据真实世界中的网络工程实践（如：数据由外到内的流向、故障排查标准步骤等）进行合理的逻辑推演。
2. **建构主义互动**：严禁教师填鸭式灌输。任何核心概念必须通过“现象 → 虚拟互动 → 请坐 → 客体化复述提炼 → 教师贴标签”来引导。
3. **字数与纯净排版**：最终逐字稿死守 950~1100 字，禁止出现 `[面带微笑]` 等废话动作，仅保留 `[板书]` 提示与阶段标题。

## 渐进式工作流 (Progressive Workflow)

当收到用户的试讲课题或材料时，请**严格按照以下两个步骤依次执行**。切勿一次性读取所有策略文件。

### Step 1: 组装教学设计骨架 (Lesson Design)

这是生成逐字稿的前置必经环节。

1. **阅读引擎核心**：首先读取 `Lesson-Design-Engine/Lesson_Design_Prompt_V6.md` 和 `Lesson-Design-Engine/Content_Selection_Strategy.md`。
2. **按需加载策略**：根据课题性质，从 `Strategy-Library/` 中**选择性加载 2~4 个最相关的策略模块**（例如理论课选 Explanation，实操课选 Practice）。**不要全部读取！**
   - *可用策略*：`Introduction-Strategy.md` (导入), `Questioning_Strategy.md` (提问), `Interaction_Strategy.md` (互动), `Explanation_Strategy.md` (讲解), `Transition_Strategy.md` (过渡), `Blackboard_Strategy.md` (板书), `Practice_Strategy.md` (练习), `Evaluation_Strategy.md` (评价), `Closing_Strategy.md` (总结)。
3. **执行**：输出完整的 5 步教学设计装配图。

### Step 2: 扩写考场逐字稿 (Teaching Script)

必须在 Step 1 确认完成后，方可执行此步骤。

1. **阅读标准宪法**：读取 `Prompts/逐字稿生成标准V2.0.md`。
2. **阅读执行引擎**：读取 `Prompts/Generate_Script_Prompt_V8.md`。
3. **执行**：根据 Step 1 的教案骨架，输出字数精准、互动达标、去除废话动作的 10 分钟逐字稿，并附带 Checklist。

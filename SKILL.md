# Teaching Design System (计算机网络试讲教案与逐字稿生成)

## 1. Skill 简介 (Introduction)
本技能用于帮助备考中职/高职计算机网络教师招聘面试的用户，根据提供的教材大纲或文本，利用内置的高分策略库，自动切片、组装并生成结构化的“10分钟无生试讲教案（Lesson Design）”与极限贴合考场纪律的“纯净版逐字稿（Teaching Script）”。

## 2. 渐进式披露工作流 (Progressive Disclosure Workflow)
**【严格限制】：为了保护上下文空间，绝对禁止一次性读取所有策略库和 Prompt 文件！必须遵循以下步骤，按需加载（使用 cat 等命令读取）。**

### Phase 1: 需求诊断与内容切片 (Content Selection)
- **触发时机**：当用户提供了一段教材文本或要求讲某个课题时。
- **必须读取的文件**：
  - `Lesson-Design-Engine/Content_Selection_Strategy.md`
- **执行动作**：执行大章节剪枝，提炼逻辑主线，筛选出 1-2 个硬核重难点，向用户输出“教学内容切片声明（AI诊断）”。

### Phase 2: 组装教学设计骨架 (Lesson Design Generation)
- **触发时机**：切片完成，准备规划课堂五步流程。
- **必须读取的文件**：
  - `Lesson-Design-Engine/Lesson_Design_Prompt_V6.md`
- **按需动态加载策略库（Progressive Loading）**：
  - **不要一次性读取所有策略！** 
  - 请根据这堂课的实际需求，从以下 `Strategy-Library/` 目录中挑选 2~4 个你打算使用的模块进行读取（例如：`cat Strategy-Library/Introduction-Strategy.md Strategy-Library/Explanation_Strategy.md`）。
  - **可用策略资产索引**：
    - `Introduction-Strategy.md` (导入)
    - `Questioning_Strategy.md` (提问)
    - `Interaction_Strategy.md` (互动)
    - `Explanation_Strategy.md` (讲解)
    - `Transition_Strategy.md` (过渡)
    - `Blackboard_Strategy.md` (板书)
    - `Practice_Strategy.md` (练习)
    - `Evaluation_Strategy.md` (评价)
    - `Closing_Strategy.md` (总结)
- **执行动作**：输出严格对齐 V2.0 宪法的教案骨架。

### Phase 3: 生成考场逐字稿 (Teaching Script Generation)
- **触发时机**：教案骨架（Lesson Design）生成完毕。
- **必须读取的文件**：
  - 先读最高宪法：`Prompts/逐字稿生成标准V2.0.md`
  - 再读执行引擎：`Prompts/Generate_Script_Prompt_V8.md`
- **执行动作**：生成 950~1100 字的“极净版 / 引导建构式 / 客体化复述 / 符合现实工程逻辑”的 10 分钟逐字稿，并附带 Checklist 报告。

## 3. 核心纪律总结 (Core Directives)
- **现实工程与常识优先**：在构建教案与话术逻辑时，严禁盲目顺从教材的字面排版顺序。必须引导虚拟学生根据真实世界中的网络工程实践（如：数据流向、协议层次依赖、排错思路等）进行合理的逻辑推演。
- **建构主义互动**：严禁教师进行填鸭式灌输，必须通过“现象 → 虚拟互动 → 请坐 → 客体化复述提炼 → 教师贴标签”来推进教学。
- **纯净排版**：逐字稿禁止出现 `[面带微笑]` 等废话动作，仅保留分块标题和 `[板书]` 提示，且总讲话字数死守 950~1100 字。

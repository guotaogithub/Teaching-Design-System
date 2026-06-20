# Practice Strategy (V2)

本练习策略库专为 10 分钟无生试讲设计。巩固练习环节的核心定位是**轻量快速**：用约 45 秒完成一道简短习题的问答，快速验证学生对重点知识的掌握，然后把宝贵时间留给新课讲授。

**选题原则**：优先选择"快速判断/简答"类策略（编号 PRA-Q 开头），题目一句话出完、学生一句话答完、教师一句话收束。仅当课题本身以实操为核心（如组网实验课）时，才考虑使用"实操排错"类策略（编号 PRA-E 开头），但仍需控制在 45 秒以内。

---

## Quick-Fire Strategies（快速问答类，首选）

### PRA-Q1. Quick True-or-False Judgment (快速判断对错策略)
- **Recommendation**: ★★★★★
- **Purpose**: 用一句判断题快速检验学生是否掌握本节核心概念，45 秒内完成出题、回答、反馈全流程。
- **Teaching Stage**: 巩固练习 (Consolidation)
- **Template**: "我来出一道判断题考考大家：[一句话命题]，对还是错？[点名]，你来判断。"
- **Network Example**: "判断题：'波特率和比特率在任何情况下数值都相等'，对还是错？第三排的同学。——请坐，判断正确，只有当每个码元恰好携带 1 比特时两者才相等，否则比特率是波特率的整数倍。"
- **Risk**: 命题过于简单变成送分题，失去检验价值；命题应聚焦本节易混淆点。
- **Difficulty**: Low (低)

### PRA-Q2. One-Sentence Concept Recall (一句话概念回忆策略)
- **Recommendation**: ★★★★★
- **Purpose**: 让学生用一句话复述本节最核心的结论或定义，快速确认理解到位。
- **Teaching Stage**: 巩固练习 (Consolidation)
- **Template**: "最后检验一下，谁能用一句话告诉我[核心问题]？[点名]。"
- **Network Example**: "谁能用一句话说清楚 VLAN 的本质作用？课代表。——请坐，概括得很准确，VLAN 就是在一台物理交换机上划出多个逻辑上隔离的广播域。"
- **Risk**: 学生回答过于冗长时教师需果断收束，避免拖时间。
- **Difficulty**: Low (低)

### PRA-Q3. Quick Scenario Choice (快速场景选择策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 给出一个极短的应用场景，让学生快速选择应使用哪个概念或技术，检验知识迁移能力。
- **Teaching Stage**: 巩固练习 (Consolidation)
- **Template**: "快速抢答：[一句话场景描述]，这种情况应该用[选项A]还是[选项B]？"
- **Network Example**: "视频会议对实时性要求很高，偶尔丢几个包也没关系，这种场景应该用 TCP 还是 UDP？第一排的同学。——请坐，回答正确，UDP 牺牲可靠性换取低延迟，正好适合实时音视频。"
- **Risk**: 场景描述过长会拖慢节奏；必须控制在一句话以内。
- **Difficulty**: Low (低)

---

## Engineering Drill Strategies（实操排错类，仅实操课题使用）

以下策略适用于课题本身以网络配置、组网实验为核心的试讲。使用时仍需控制在 45 秒以内，聚焦单一错误点，快速诊断收束。

---

### PRA-E1. Typical Configuration Error Diagnosis Patrol (典型配置错误巡视纠偏策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 通过虚拟"发现"学生高频配置错误，展现教师对工程误区的预判与即时纠偏能力。
- **Teaching Stage**: 巩固练习 (Consolidation), 实验实操 (Hands-on Practice)
- **Template**: "老师在巡视时发现这位同学的配置有个典型问题，大家一起来看……"
- **Network Example**: "这位同学的子网掩码写成了 255.255.255.255，数据包根本找不到网关。掩码应该设为 24 位，对不对？"
- **Risk**: 纠偏时间过长导致练习环节超时；需控制在 30 秒内完成诊断与纠正。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Error Message Diagnosis Interaction (互动)

### PRA-E2. Ping Test Connectivity Verification Strategy (Ping测试连通性验证策略)
- **Recommendation**: ★★★☆☆
- **Purpose**: 将 Ping 命令转化为可视化的链路排查过程，通过单方面推演数据流，验证链路通断逻辑。
- **Teaching Stage**: 实验实操 (Hands-on Practice), 难点突破 (Breakthrough of Difficulties)
- **Template**: "Ping 不通？我们顺着路径倒推：本端有没有 IP？网关通不通？路由表有没有下一跳？"
- **Risk**: 排查步骤过多容易超时；聚焦单一故障点即可。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Process Slicing & Step-by-Step Deduction (讲解)

### PRA-E3. CLI Syntax & Logic Debugging Patrol (命令行语法与逻辑指导策略)
- **Recommendation**: ★★★☆☆
- **Purpose**: 模拟因语法错误导致的命令行失效，引导学生检查配置逻辑与语境。
- **Teaching Stage**: 实验实操 (Hands-on Practice)
- **Template**: "这位同学在用户视图下就想配 IP 地址，系统当然识别不了。得先进入接口视图才行。"
- **Risk**: 应聚焦高频工程痛点（如视图切换），不展示冷门拼写错误。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Command Line Execution Interaction (互动)

### PRA-E4. Topology Link & Port Mode Verification Patrol (拓扑连线与端口模式验证策略)
- **Recommendation**: ★★★☆☆
- **Purpose**: 模拟拓扑搭建过程中的基础连线与逻辑错误，确保学生建立正确的组网规范意识。
- **Teaching Stage**: 实验实操 (Hands-on Practice)
- **Template**: "连线没问题，为什么 VLAN 数据传不过去？检查端口模式——Access 口不能传带标签的帧，得改成 Trunk。"
- **Risk**: 仅适用于涉及交换机配置的课题；非实操课题不要使用。
- **Difficulty**: High (高)
- **Compatible Strategy**: Topology Fault Correction Interaction (互动)

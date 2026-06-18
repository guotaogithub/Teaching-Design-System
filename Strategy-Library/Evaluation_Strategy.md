# Evaluation Strategy (V1)

本评价策略库专为 10 分钟无生试讲设计，旨在通过精准、专业的反馈话术，提升课堂的工程素养与学术深度。
严格剔除低效的泛泛表扬（如“很好”、“正确”），转而聚焦于学生的排错思路、工程规范、观察敏锐度及知识迁移能力，确保评价对后续教学具有导向意义。

---

## 1. Engineering Logic Praise Strategy (工程逻辑赞赏策略 - 完全正确场景)
- **Recommendation**: ★★★★★
- **Purpose**: 超越结果正确性，将评价拔高到对学生专业工程思维、系统排错逻辑的肯定。
- **Target Scenario**: 学生给出了完美的、符合规范的解决方案或排错方案。
- **Template**: “这位同学不仅找出了错误，更难得的是他的排错思路是从底向上逐层排查的，这种严谨的工程思维非常值得大家学习。谁能总结一下，为什么他的方法比直接替换设备更高效？”
- **Network Example**: “A同学不仅一眼看出是VLAN配置错了，还提出了用Trunk链路透传的根本解决方案，这种全局组网意识非常棒！这正是网络工程师在面对复杂分支机构组网时最核心的能力。”
- **Action/Visual Support**: 面带赞赏的微笑点头，右手手心向上做出请坐的动作，转身在黑板左侧板书该同学提到的关键词（如“Trunk”、“全局观”），增加评价的视觉分量。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Process Slicing & Step-by-Step Deduction (讲解), Troubleshooting/Disaster Recovery Transition Strategy (过渡)

## 2. Constructive Precision Correction Strategy (工程精准修补策略 - 部分正确场景)
- **Recommendation**: ★★★★★
- **Purpose**: 在肯定核心思路的基础上，精准指正细微的配置瑕疵，将评价转化为二次强化知识点的契机。
- **Target Scenario**: 学生回答逻辑大方向正确，但存在参数错误、术语不规范或参数冗余等瑕疵。
- **Template**: “你的大思路完全准确，确实需要配置访问控制。不过，你刚才提到的ACL参数，在企业级生产环境下是否有点过于粗糙？如果我们要进一步收紧安全策略，应该在哪里做精细化限制？”
- **Network Example**: “思路对头，确实应该用NAT。但你刚才配置的地址池是动态的，对于企业服务器出口，我们通常建议配置静态NAT，为什么？这就涉及到了外网访问的稳定性。把这个参数细化一下，你的方案就非常完美了。”
- **Action/Visual Support**: 身体略微向学生方向倾斜，眼神温和地进行眼神交流，左手做出“修补、细化”的动作（如手指做画图补齐动作），右手在黑板上修正具体的参数。
- **Difficulty**: High (高)
- **Compatible Strategy**: Error Message Diagnosis Interaction (互动), Precision Correction Questioning (提问)

## 3. Path-Correction Guidance Strategy (故障路径引导策略 - 完全错误/卡壳场景)
- **Recommendation**: ★★★★☆
- **Purpose**: 避免直接否定，而是通过拆解问题、提供阶梯式线索，帮助学生主动发现故障源，完成自我否定与重构。
- **Target Scenario**: 学生完全卡壳，或者提出的方案逻辑错误严重，无法继续进行。
- **Template**: “卡住了吗？没关系，这是每一个网络工程师都会经历的过程。我们先不看最终结果，我们回退一步：如果 Ping 不通网关，你的第一步应该检查什么配置？从这个节点开始推演，你现在能看到什么异常？”
- **Network Example**: “先别急着修改路由表。我们回到二层链路，看一下这个端口灯亮没亮？如果物理层都不同，再复杂的路由配置也只是纸上谈兵。从物理层、数据链路层到网络层，咱们一层层排查。”
- **Action/Visual Support**: 眼神充满鼓励，身体姿态放松，双手做出“层层拆解、引导”的姿态（类似扒开层层障碍），指引学生关注黑板上的协议栈框架（分层骨架）。
- **Difficulty**: High (高)
- **Compatible Strategy**: Protocol Stack Layered Scaffolding Board Strategy (板书), Troubleshooting/Disaster Recovery Transition Strategy (过渡)

## 4. Engineering Standardization Praise Strategy (工程化规范肯定策略 - 观察敏锐/规范场景)
- **Recommendation**: ★★★★☆
- **Purpose**: 表扬学生在实操过程中表现出的工程严谨性、文档习惯或对细节的敏锐观察，强调规范胜于技巧。
- **Target Scenario**: 学生在实操或互动中表现出极佳的观察力，或使用了非常标准、严谨的工程操作习惯。
- **Template**: “非常敏锐！很多同学在配置时往往忽略了这些细小的报错信息，但这位同学第一时间捕捉到了模拟器的这条警告，这就是一名优秀的网络运维人员最宝贵的职业敏感度。”
- **Network Example**: “注意这位同学配置命令行时的习惯，每个接口都添加了 `description` 描述，这在真实的大型网络中是极其重要的文档规范！大家在以后的实操中，一定要把这种良好的工程习惯坚持下去。”
- **Action/Visual Support**: 点头称赞，双手抱胸点头，随后双手大方地示意全班向该同学看齐，在黑板“工程规范”栏中记下重点。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Topology & Business Mapping (讲解), Practice Strategy (实操)

## 5. Reflection-Triggering Evaluation Strategy (反思驱动型评价策略 - 过程性评价)
- **Recommendation**: ★★★★☆
- **Purpose**: 将评价过程转变为反思过程，引导学生思考如果场景变更，方案如何调整，拓展思维广度。
- **Target Scenario**: 学生回答正确后，立即追问，推动其进行迁移思考。
- **Template**: “这个方案完美解决了当前的问题。现在我增加一个条件：如果企业的业务流量增加十倍，你的配置依然能保证不丢包吗？你的方案的扩展性如何？”
- **Network Example**: “很好，ACL 完美拦截了非授权访问。但如果明天公司接入了新的分公司，这个 ACL 规则如何同步？我们是否需要通过集中式的安全管理平台来下发策略？这种动态扩展能力，是网络规划的下一阶段重点。”
- **Action/Visual Support**: 眉头微挑，眼神透出期待，手指轻轻敲击黑板上的方案位置，做出“思考、拓展”的引导手势，身体向后撤一步，给学生留出思考空间。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Scale/Complexity Upgrade Transition Strategy (过渡), Cognitive Conflict Questioning (提问)

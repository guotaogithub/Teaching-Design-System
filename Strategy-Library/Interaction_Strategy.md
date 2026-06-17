# Interaction Strategy Library (V2)

本互动策略库专为 10 分钟无生试讲设计，仅保留 30~60 秒内可完成的师生微互动与虚拟实操策略。
所有字段均已结构化，对齐 Questioning Strategy V2 标准，作为 Teaching Design Engine 的可调用组件。

---

## 1. Error Message Diagnosis Interaction (报错信息诊断互动)
- **Recommendation**: ★★★★★
- **Purpose**: 培养网络工程排错思维，通过模拟真实故障现象，训练学生将错误表现与协议原理精准对应。
- **When to Use**: 讲解过协议配置要点、命令行操作或抓包分析之后，进行短平快诊断练习时。
- **Teaching Stage**: 巩固练习 (Consolidation), 难点突破 (Breakthrough of Difficulties)
- **Template**: “各位同学请看大屏幕，这是一段我们刚刚模拟截获的网络报错信息/抓包报文。你发现了什么异常？哪位同学能迅速指出故障点并给出修复思路？”
- **Network Example**: “大家看Wireshark抓包里这个被标记为黑色的报文，TCP Flags里竟然只有RST位被置位了。哪位同学能判断一下，这说明通信过程中遇到了什么严重问题，是谁单方面中断了连接？”
- **Expected Student Response**: 能够根据报错码或置位状态（如 RST）迅速判断出故障根源（如连接被强制重置），并提出重启流程或检查策略的解决思路。
- **Risk**: 若诊断素材过难或过偏，学生无法找到切入点，会导致试讲冷场；务必选用特征明显、与刚讲知识直接对应的典型错误截图。
- **Difficulty**: High (高)
- **Compatible Strategy**: Diagnostic Questioning, Scenario-based Questioning

## 2. Topology Fault Correction Interaction (网络拓扑排错互动)
- **Recommendation**: ★★★★★
- **Purpose**: 强化学生对组网规范与设备逻辑的全局审视能力，杜绝凭空记忆。
- **When to Use**: 多媒体屏幕上展示一幅含有隐性错误的网络拓扑图，用于检验学生知识掌握情况。
- **Teaching Stage**: 新知探究 (New Knowledge Exploration), 巩固练习 (Consolidation)
- **Template**: “请大家检查屏幕上这张拓扑图，里面隐藏了一个逻辑上或配置上的小陷阱。给大家30秒时间观察，哪位火眼金睛先来挑刺？”
- **Network Example**: “看这张企业网络拓扑图，左侧核心交换机下挂了两台PC，我明明写着属于VLAN 10和VLAN 20。但大家注意，中间这条级联链路是什么端口类型？就靠这条Access端口，VLAN 20的数据能带着标签到达对端吗？”
- **Expected Student Response**: 能够迅速指出其中一台交换机配置了错误的端口模式（如应为Trunk却配成了Access），并推理出故障后果（VLAN标签被剥离/丢弃）。
- **Risk**: 陷阱过于隐蔽，超出学生当前认知水平；需控制明显程度，将错误聚焦在刚讲过的重点配置参数上。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Follow-up Questioning

## 3. Protocol/Architecture Filling Interaction (协议/架构补全互动)
- **Recommendation**: ★★★★☆
- **Purpose**: 打破单向灌输，快速检验核心术语的瞬时记忆，确保学生掌握协议的模块封装与架构层次。
- **When to Use**: 汇总概念特征、对比表格、关键步骤流程等高度结构化内容的巩固阶段。
- **Teaching Stage**: 巩固练习 (Consolidation)
- **Template**: “这是[协议/架构]的模块封装空白表。我们在分析过程中，此处[具体层级/字段]缺失了。哪位同学能根据我们刚才梳理的规范，把这个协议字段填充完整？”
- **Network Example**: “请看这张TCP报文首部格式结构图，现在老师隐藏了‘源端口号’和‘目的端口号’。请问，当客户端发起网页请求时，目的端口字段应当填充什么标准协议号？”
- **Expected Student Response**: 准确回答出缺失的模块名称或标准数字（如 80, 443 端口）及核心协议字段（如 Sequence Number）。
- **Risk**: 避免变成单调的背诵；应选取最易混淆或需强化的盲点进行结构化填充，并强调其工程意义。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Summarizing Questioning

## 4. Connect Device Interaction (连接设备拟真连线互动)
- **Recommendation**: ★★★★☆
- **Purpose**: 将设备连接知识转化为主体性动手操作，对抗网络设备概念抽象难记的问题。
- **When to Use**: 讲解交换路由组网、或是广域网接入场景的初建认知环节。
- **Teaching Stage**: 新知探究 (New Knowledge Exploration)
- **Template**: “现在大屏幕上出现了几个孤立的设备图标，比如路由器、交换机、防火墙和外网云。谁上来试着用手指给大家划一条线，告诉我广域网出口这条链路该接哪个设备的哪个口？”
- **Network Example**: “这里是一台核心交换机、一台路由器和一台宽带光猫。哪位同学愿意来大屏上画条线，告诉我这三台设备之间需要用怎样的线缆相连？如果企业要连外网，光猫的网口应该指向谁的WAN口？”
- **Expected Student Response**: 能够虚拟连线正确（交换机→路由器LAN口→光猫指向路由器WAN口），并说出端口类型（如 RJ45/光口）。
- **Risk**: 交互痕迹无法在无生试讲中由学生真实完成；教师需要通过“自演自画”描绘鼠标/手指移动轨迹，并在画完后立即给出口头确认。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Prediction Questioning

## 5. Command Line Execution Interaction (命令行推演互动)
- **Recommendation**: ★★★☆☆
- **Purpose**: 提升实战与职业感，在设备配置过程中引导学生思考命令语法与输出结果，验证配置逻辑。
- **When to Use**: 教师在模拟器中输入命令前半段或敲下回车验证配置前。
- **Teaching Stage**: 实验演示 (Experiment/Demonstration), 难点突破 (Breakthrough of Difficulties)
- **Template**: “目前我们已经进入了[特定配置模式]。接下来我要配置[特定功能]，命令的前半部分是[命令片段]，后面的关键参数大家觉得应该补上什么？/ 敲下回车后，大家预测一下[相关状态]会发生怎样的变化？”
- **Network Example**: “现在我们已经在接口视图下输入了 `ip address 192.168.1.1`，后面还需要补全什么参数才能让设备识别网络规模？如果我现在敲回车，这条直连路由会自动出现在路由表中吗？”
- **Expected Student Response**: 能补充完整的命令后缀（如 `255.255.255.0` 或子网掩码长度），并对执行结果做出合理预测。
- **Risk**: 学生可能对命令语法遗忘导致回答卡壳，教师应利用 Tab 补全提示或错误提示信息来引导纠正，避免单纯等待答案。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Follow-up Questioning, Prediction Questioning

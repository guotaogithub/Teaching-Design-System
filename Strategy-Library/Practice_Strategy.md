# Practice Strategy (V1)

本练习策略库专为 10 分钟无生试讲设计，聚焦在虚拟练习环节中，通过教师单方面实演，精准刻画出虚拟学生在实操中遇到的具体技术问题与即时纠偏，杜绝无意义的等待与空洞的话术。
所有字段均已结构化，`Action/Visual Support` 字段专门指导试讲过程中的教师巡视走位与肢体配合。

---

## 1. Typical Configuration Error Diagnosis Patrol (典型配置错误巡视纠偏策略)
- **Recommendation**: ★★★★★
- **Purpose**: 打破练习环节的冷场，通过虚拟“发现”学生高频配置错误，展现教师对工程误区的预判与即时纠偏能力。
- **Teaching Stage**: 巩固练习 (Consolidation), 实验实操 (Hands-on Practice)
- **Template**: “老师在巡视时发现第四组的一位同学配置出现了个小插曲，大家先停一下，我们一起来看下他的屏幕，这个错误非常典型，相信很多同学都容易忽略...”
- **Network Example**: “你看这位同学的 PC IP 配置了 192.168.1.10，子网掩码却写成了 255.255.255.255。这会导致数据包根本找不到网关！记住，掩码决定了同网段的范围。这位同学马上改一下，掩码是不是应该设为 24 位？”
- **Action/Visual Support**: 教师假装从讲台走下，轻快步履走向教室一侧，身体微微前倾，假装注视某位学生的屏幕，右手食指指向屏幕特定位置，神情专注且鼓励。
- **Risk**: 纠偏时间过长导致练习环节超时；需控制在 30 秒内完成诊断与纠正。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Error Message Diagnosis Interaction (互动)

## 2. Ping Test Connectivity Verification Strategy (Ping测试连通性验证策略)
- **Purpose**: 将抽象的 Ping 命令转化为可视化的链路排查过程，通过单方面推演数据流，验证链路通断逻辑。
- **Teaching Stage**: 实验实操 (Hands-on Practice), 难点突破 (Breakthrough of Difficulties)
- **Template**: “大家测试链路通了吗？老师看到有些同学 Ping 出来显示 'Request Timed Out'。别急，我们顺着路径倒推：先看本端有没有 IP？再看网关通不通？如果是跨网段，路由表有没有下一跳地址？”
- **Network Example**: “现在 Ping 不通，是因为 ARP 表项没有建立成功吗？或者是对端主机禁 Ping 了？大家在模拟器命令行里输入 `display arp`，看看对应的 MAC 地址有没有学到。如果没学到，那问题就定位在二层链路！”
- **Action/Visual Support**: 教师做出在键盘上快速敲击的动作，眼神在黑板的拓扑图与课件模拟器之间切换，左手做“追踪路径”的滑动动作，示意数据包的流转。
- **Risk**: 过于机械地念 Ping 的输出结果，显得像在朗读；应重点突出排查的逻辑链条。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Troubleshooting/Disaster Recovery Transition Strategy (过渡), Process Slicing & Step-by-Step Deduction (讲解)

## 3. CLI Syntax & Logic Debugging Patrol (命令行语法与逻辑指导策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 模拟在模拟器中操作时，因语法错误导致的命令行失效，引导学生检查配置逻辑与语境。
- **Teaching Stage**: 实验实操 (Hands-on Practice)
- **Template**: “老师看到有位同学输入接口配置命令时报错了。在系统视图下，我们得先进入具体端口才能敲 IP，直接敲命令系统当然识别不了。大家看屏幕，这种语法错误，模拟器会直接给出反馈，我们一定要看报错提示！”
- **Network Example**: “这里报错 'Invalid command'，仔细看，你是不是在用户视图模式下就想配 IP 地址了？得先 `interface GigabitEthernet 0/0/1` 进入接口才行！记住命令运行的语境（Context），这是网络工程师的基本功。”
- **Action/Visual Support**: 教师做出皱眉、摇头纠正学生错误的动作，随后神情转为舒缓并做出“输入命令”的手势，指引学生看命令行语法规范。
- **Risk**: 不宜展示过于冷门的命令拼写错误；应聚焦于模式错误（如视图切换）等高频工程痛点。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Command Line Execution Interaction (互动)

## 4. Topology Link & Port Mode Verification Patrol (拓扑连线与端口模式验证策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 模拟拓扑搭建过程中的基础连线与逻辑错误，确保学生建立正确的组网规范意识。
- **Teaching Stage**: 实验实操 (Hands-on Practice)
- **Template**: “大家看这张拓扑，连线没问题，为什么 VLAN 20 还是传不过去？检查一下级联链路的端口模式！我看到第二组同学的交换机端口配的是 Access，这怎么能传带标签的 VLAN 数据？”
- **Network Example**: “记住，连接多 VLAN 的链路，端口模式必须配置为 Trunk！这就像给货物贴上标签，没有 Trunk 通道，交换机收到带标签的帧直接就丢弃了。马上把这几个口配成 `port link-type trunk`，配置马上生效！”
- **Action/Visual Support**: 教师手持电子笔，在黑板拓扑图上画出级联链路，用右手食指重重地点出链路端口位置，示意学生重点检查此处，眼神坚定且自信。
- **Risk**: 若拓扑图画得过于简单，学生看不出端口错误逻辑；需在黑板上清晰标注端口标识（如 G0/0/1）。
- **Difficulty**: High (高)
- **Compatible Strategy**: Topology Fault Correction Interaction (互动), Main-Sub Dual-Zone Topology Board Strategy (板书)

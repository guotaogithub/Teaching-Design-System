# Interaction Strategy (V1)

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

## 3. Blank Filling Arcade Interaction (课件填空接龙互动)
- **Recommendation**: ★★★★☆
- **Purpose**: 打破单向灌输，快速检验核心术语的瞬时记忆，确保学生跟紧教学节奏。
- **When to Use**: 汇总概念特征、对比表格、关键步骤流程等高度结构化内容的巩固阶段。
- **Teaching Stage**: 巩固练习 (Consolidation)
- **Template**: “这是OSI模型/TCP首部格式的空白表，老师点到哪一格，大家就一起帮我把答案补充完整！来，传输层这块对应的那个关键字段是什么？”
- **Network Example**: “请看这张TCP报文首部格式结构图，现在老师把里面的‘源端口号’和‘目的端口号’全擦掉了。我指着第一行问，客户端发起网页请求时，它这里的目的端口通常会填什么知名数字？”
- **Expected Student Response**: 全班齐答或个别抢答出标准端口号（如 80, 443）及核心协议字段（如 Sequence Number）。
- **Risk**: 避免变成单调的复读游戏；应选取最易混淆或需强化的盲点进行随机填空，并伴有短评。
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

## 5. Find the Difference Observation Interaction (找茬观察互动)
- **Recommendation**: ★★★☆☆
- **Purpose**: 通过视觉集中对比，快速区分形似实异的核心概念。
- **When to Use**: 讲解容易混淆的协议报文格式、设备外观或通讯流程等具有对照价值的环节。
- **Teaching Stage**: 新知探究 (New Knowledge Exploration)
- **Template**: “屏幕左边是[A]发出的广播报文，右边是[B]发出的单播报文。请大家盯着这两张图仔细看30秒，看谁第一个发现目标MAC地址这一项里，藏着什么截然不同的特征？”
- **Network Example**: “右边这个AR P请求报文和右边这个普通IP数据包，请大家聚焦二层帧头的Destination MAC这一栏。谁发现了？为什么ARP请求里填的是‘FF-FF-FF-FF-FF-FF’这个奇怪的全F广播地址？”
- **Expected Student Response**: 快速指出ARP请求的目标MAC为广播地址，并解释因为此时发送方不知道目标设备的硬件地址。
- **Risk**: 容易和对比提问混淆，需强调“视觉发现”而非“听讲理解”；建议直接配高清对齐的概念对比图。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Comparative Questioning

## 6. Flash Q&A Interaction (闪卡快问快答互动)
- **Recommendation**: ★★★☆☆
- **Purpose**: 极速激活课堂氛围，用于复习前一节课或上一环节的高频指令和缩略词。
- **When to Use**: 课堂导入的暖场环节，或者在长时间单向讲解后重新捕捉注意力。
- **Teaching Stage**: 课堂导入 (Introduction), 巩固练习 (Consolidation)
- **Template**: “来，30秒热身赛开始！老师指到哪个词，大家就光速报它的全称或作用。准备好了吗？第一个：DNS！”
- **Network Example**: “今天我们要进阶学路由了，但先来热热身！看词条：HTTP, NAT, DHCP, ARP, ICMP。老师指到哪，你就给老师秒回它叫什么全称！好，第三个词——DHCP，给老师你的答案！”
- **Expected Student Response**: 迅速反应，齐声或指定回答出准确的全称及简短核心功能描述。
- **Risk**: 语速控制不当易自乱阵脚，教师需用“拍手/敲屏”等信号统一答题节奏；避免用太难或太偏的单词冷场。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Follow-up Questioning

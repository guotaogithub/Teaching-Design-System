# Blackboard Strategy (V1)

本板书策略库专为 10 分钟无生试讲设计，聚焦"边讲边写、动态生成"的黑板书写策略。
严格剔除课前预制全板、脱离讲解的大段抄写等低效板书行为。
所有字段均已结构化，对齐 Teaching Design Engine 可调用标准，确保布局、时机与内容可被直接提取。

---

## 1. Main-Sub Dual-Zone Topology Board Strategy (主副双区拓扑板书策略)
- **Recommendation**: ★★★★★
- **Purpose**: 左侧留存课堂知识骨架，右侧提供动态推演空间，兼顾结构化记忆与过程性思维展示。
- **Layout Type**: 黑板左侧 60% 为主板书区（知识提纲/层级标题），右侧 40% 为副板书区（动态拓扑草图/协议字段/临时推演）。两个区域功能分离，互不覆盖。
- **Execution Timing**: 开课 30 秒内在主板书区写下本节核心标题与一级提纲（2~3 个关键词即可）；讲解过程中每次涉及拓扑、字段、流程时，转身在副板书区边说边画，单次书写不超过 5 秒。副板书区内容可随讲解推进擦除或覆盖。
- **Network Example**: 主板书区写"VLAN 技术 → 隔离原理 → Trunk 配置"三级提纲。讲解隔离原理时，在副板书区画一台交换机简图，中间画一条竖虚线，左右分别标"VLAN 10 / VLAN 20"。讲到 Trunk 时，在副板书区追加一条跨交换机的链路，标注"802.1Q Tag"。
- **Risk**: 副板书区空间不足导致后续内容无处书写；需在设计阶段预判副板书使用次数，必要时用板擦局部清理腾出空间。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Process Slicing & Step-by-Step Deduction (讲解), Topology Fault Correction Interaction (互动)

## 2. Protocol Stack Layered Scaffolding Board Strategy (协议栈分层脚手架板书策略)
- **Recommendation**: ★★★★★
- **Purpose**: 将 OSI/TCP-IP 协议栈作为固定板书骨架，逐层填充讲解内容，让学生始终看到当前知识在整体架构中的位置。
- **Layout Type**: 黑板中央纵向排列 4~5 层水平横线，每层代表一个协议层级（如应用层、传输层、网络层、数据链路层、物理层），形成"脚手架"结构。各层留白，随讲解逐层填写。
- **Execution Timing**: 开课 45 秒内用直尺或徒手快速画出分层横线框架（仅画线和层名，不填内容）。每讲到一个协议层时，转身在对应层的横线上方/下方填写核心协议名或关键字段，单次 3~5 秒。整个课堂结束时，板书自然形成完整的协议栈全景图。
- **Network Example**: 画五层横线后，在应用层写"HTTP / DNS"；讲到传输层时填写"TCP（可靠）/ UDP（高效）"并用箭头标注"三次握手"；讲到网络层时写"IP 寻址 + TTL 防环"。最终板书呈现一个从上到下逐步填满的协议栈知识图谱。
- **Risk**: 框架层数过多（如完整七层）导致每层空间过窄，字迹拥挤难辨；建议根据课程内容裁剪为 4~5 层，合并底层或简化不涉及的层。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Protocol/Architecture Filling Interaction (互动), Contrast & Boundary Definition (讲解)

## 3. Comparison Table Progressive Fill Board Strategy (对比表格渐进填充板书策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 用结构化表格对比易混淆技术，通过渐进填写避免信息过载，强化辨析记忆。
- **Layout Type**: 黑板右侧绘制 2~3 列对比表格，列头为对比维度（如"TCP vs UDP"），行为关键属性（如"连接方式"、"可靠性"、"速度"、"典型应用"）。表格先画空壳，内容逐行填写。
- **Execution Timing**: 在讲解进入对比环节的瞬间（通常在新知探究后半段），转身用 5 秒画出表格框架和列头。每分析完一个维度，在对应单元格填写结论，单次 3 秒。最后一行可留给学生口头补全作为互动。
- **Network Example**: 表格列头为"TCP"和"UDP"。讲连接方式时，左格写"面向连接（三次握手）"，右格写"无连接"。讲可靠性时，左格写"可靠（确认+重传）"，右格写"不可靠（尽力交付）"。讲典型应用时，左格写"HTTP/FTP"，右格写"DNS/视频流"。
- **Risk**: 表格绘制不规整（列宽不一、行高参差）影响专业感；建议提前练习快速徒手画表的节奏，保持行列对齐。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Contrast & Boundary Definition (讲解), Connect Device Interaction (互动)

## 4. Data Flow Arrow Trace Board Strategy (数据流箭头追踪板书策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 用动态绘制的箭头链路模拟数据包在网络中的真实流转路径，将抽象通信过程可视化为可追踪的图形叙事。
- **Layout Type**: 黑板中央偏左绘制简化的网络拓扑（2~3 台设备图标 + 连线），右侧预留文字注释区。核心内容通过逐步绘制带方向的箭头来呈现数据流向。
- **Execution Timing**: 在讲解数据封装/传输/路由转发等流程性知识时，先用 3 秒画出设备简图。每讲一个传输步骤，用 2~3 秒画出一段箭头，并在箭头旁标注协议名或关键操作（如"SYN"、"ARP 请求"）。箭头链路随讲解逐步延伸，形成完整的通信路径。
- **Network Example**: 画 PC → 交换机 → 路由器 → 服务器的拓扑。讲 ARP 时，从 PC 画一条虚线箭头指向交换机，旁注"ARP Request（广播）"。讲路由转发时，从路由器画箭头指向服务器，旁注"查路由表 → 最长前缀匹配"。讲回程时，反向画箭头旁注"ARP Reply（单播）"。
- **Risk**: 箭头方向画反或设备位置不合理导致后续路径交叉混乱；建议在设计阶段规划好设备间距和箭头走向，预留足够空间避免线条重叠。
- **Difficulty**: High (高)
- **Compatible Strategy**: Process Slicing & Step-by-Step Deduction (讲解), Command Line Execution Interaction (互动)

## 5. Problem-Solution Dual Column Board Strategy (问题-方案双栏推演板书策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 将课堂重难点以"问题 → 方案"的双栏结构呈现，左侧暴露真实网络故障或需求，右侧逐步推导解决方案，培养工程排错思维。
- **Layout Type**: 黑板分为左右两栏，左侧栏标题为"问题/现象"，右侧栏标题为"方案/原理"。两栏内容一一对应，形成因果推演链。每对问题-方案用横线分隔，保持视觉层次。
- **Execution Timing**: 在课堂引入真实故障场景或企业需求时，先用 4 秒在左侧栏写下问题现象（如"VLAN 间无法通信"）。引导分析后，转身用 3~4 秒在右侧栏对应位置写出解决方案（如"配置三层交换/SVI 实现跨 VLAN 路由"）。每推导一对，用横线分隔，继续下一对。
- **Network Example**: 左栏依次写："① VLAN 间 ping 不通"、"② 广播风暴频繁"、"③ 外网访问时断时续"。右栏对应写："① 缺少三层路由 → 配置 SVI 网关"、"② 未启用 STP → 配置生成树协议"、"③ NAT 地址池耗尽 → 扩展 PAT 映射"。最终板书呈现一张完整的"问题排查-解决"知识图谱。
- **Risk**: 左右栏书写节奏不同步（问题写了三个，方案只写了一个）导致板书失衡；教师需在设计阶段严格配对，讲解时控制左右交替书写的频率。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Error Message Diagnosis Interaction (互动), Life/Business Analogy Explanation (讲解)

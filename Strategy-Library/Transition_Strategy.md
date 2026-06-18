# Transition Strategy (V1)

本过渡策略库专为 10 分钟无生试讲设计，旨在通过逻辑驱动、工程痛点与技术演进视角，实现各教学环节的无缝衔接。
绝对剔除机械式、形式化的过渡语言，确保每一处转折均指向真实的计算机网络工程场景与学习进阶需求。

---

## 1. Scale/Complexity Upgrade Transition Strategy (规模/复杂度升级过渡策略)
- **Recommendation**: ★★★★★
- **Purpose**: 通过打破现有技术的完美状态，制造规模化应用的痛点，自然引出进阶技术或复杂架构。
- **Connection**: 基础原理讲解环节 → 复杂组网/大规模网络实施环节
- **Template**: “刚才我们用[简单场景]实现了[功能]，这在单机或小规模实验中确实高效。但如果把这个模型扩展到真实的企业级网络，面对成百上千台终端时，刚才的方法还适用吗？我们来看看会遇到什么问题...”
- **Network Example**: “两台电脑通过一条交叉线直连通信，通过 ARP 广播确实没问题。但如果把这个场景扩展到拥有 500 名员工的办公楼，难道我们要拉 500 根线吗？广播风暴怎么解决？这就逼着我们必须引入交换机，并掌握 VLAN 划分技术。”
- **Risk**: 若规模扩大的情景描绘不够紧迫，学生无法体会引入复杂技术的必要性。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Main-Sub Dual-Zone Topology Board Strategy (板书), Topology & Business Mapping (讲解)

## 2. Security/Policy Gap Transition Strategy (安全/策略空白过渡策略)
- **Recommendation**: ★★★★★
- **Purpose**: 通过揭示“联通”与“安全”之间的本质冲突，将教学重心从“连得通”平滑切换到“控得住”。
- **Connection**: 连接性测试/功能实现环节 → 网络安全/访问控制策略环节
- **Template**: “网络现在的确是通了，但通了就真的安全了吗？在实际的生产环境中，我们不仅要求数据能到达，更要求非法流量必须被阻断。我们现在的配置，能做到精准控制谁能访问服务器、谁不能访问吗？”
- **Network Example**: “大家看，通过刚才的静态路由配置，财务部的 PC 已经可以 ping 通研发部的服务器了。但在企业内部，这两者应该隔离。我们要怎么做，才能既保证网络畅通，又把财务数据的访问权限仅仅授权给合法的员工？这就需要 ACL 技术登场了。”
- **Risk**: 过渡转折过于生硬，需确保“安全”是紧接着“通畅”后的下一阶段工程必然。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Error Message Diagnosis Interaction (互动), Topology & Business Mapping (讲解)

## 3. Cognitive Conflict Transition Strategy (认知冲突演进过渡策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 通过展示真实抓包现象与预设理论的细微差距，制造认知冲突，引导学生深入探究底层机制。
- **Network Example**: [连接的教学环节，如：协议理论讲解环节 → 底层数据包分析环节]
- **Template**: “大家看，书上告诉我们[协议原理]是这样的，逻辑非常完美。但刚才我们通过抓包工具，看到的数据包头部字段却和我们推演的不太一样。为什么会有这个偏差？这里面隐藏了什么特殊的控制机制？”
- **Network Example**: “按理论，TCP 三次握手后连接就建立了。但大家看这个抓包，在连接建立后，为什么紧接着出现了一个 RST 包？这就说明实际的网络通信中，除了理论流程，还有更底层的超时/重传机制在介入。我们拆开报文详细看看。”
- **Risk**: 需要课件配合真实的抓包截图，否则会导致空中楼阁，缺乏可信度。
- **Difficulty**: High (高)
- **Compatible Strategy**: Packet Dissection & Reverse Engineering (讲解), Protocol Stack Layered Scaffolding Board Strategy (板书)

## 4. Requirement/Business Scenario Shift Transition Strategy (需求/业务场景切换过渡策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 将技术知识点封装在具体的业务需求中，通过场景的演进推动教学环节的迭代。
- **Connection**: 设备基础配置环节 → 业务功能部署环节
- **Template**: “基础的链路连接和 IP 分配我们已经搞定了，这就像把网络这台车组装好了。但车组装好了只是第一步，我们要让它去跑业务。现在企业老板给出了新的业务需求：[业务场景]，我们该如何配置现有网络来满足这个需求？”
- **Network Example**: “设备已经互联互通了。现在企业接到一个新需求：要上线一套视频会议系统。这种流量不仅延迟敏感，而且带宽占用极大。我们现有的网络配置能保证视频不卡顿吗？我们得针对这种特定业务进行 QoS 策略部署。”
- **Risk**: 业务场景如果选得过于冷门或生僻，学生难以产生共鸣。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Scenario-based Questioning (互动), Topology & Business Mapping (讲解)

## 5. Troubleshooting/Disaster Recovery Transition Strategy (排错/灾备情境过渡策略)
- **Recommendation**: ★★★★☆
- **Purpose**: 打破“一帆风顺”的教学流，引入故障场景，从“搭建者”切换视角为“运维者”，强化工程思维。
- **Connection**: 正常配置成功环节 → 网络故障诊断与优化环节
- **Template**: “配置完美运行，大家都很有成就感。但如果明天上班，核心设备突然断电，或者光纤被挖掘机挖断了，网络会发生什么？我们的配置能否自动恢复？我们来模拟一次真实的突发故障，看看网络是否有自我修复能力。”
- **Network Example**: “现在网络互通非常顺畅。假如现在这台主交换机电源被拔掉，终端的网络会中断多久？这就是高可用性（HA）的课题。我们不测不知道，一测吓一跳，现在网络切换时间高达 30 秒，我们如何通过配置把这个时间缩短到毫秒级？”
- **Risk**: 需要提前设计好故障现象，并在试讲中通过口头描述故障现象来快速带入。
- **Difficulty**: High (高)
- **Compatible Strategy**: Topology Fault Correction Interaction (互动), Problem-Solution Dual Column Board Strategy (板书)

# Questioning Strategy Library (V2)

本提问策略库专为 10 分钟无生试讲设计，作为 Teaching Design Engine 的可调用知识库。
每个策略已结构化，所有字段均服务于未来 AI 在 Teaching Design、Script 和 Prompt 的自动生成。

---

## 1. Prediction Questioning (预测提问)
- **Recommendation**: ★★★★★
- **Purpose**: 引发前置思考，建立假设，为后续的验证（实验/抓包）做铺垫，强化逻辑推导能力。
- **When to Use**: 在讲解核心原理或操作验证之前，需要学生带着悬念进入下一步。
- **Teaching Stage**: 新知探究 (New Knowledge Exploration), 实验演示 (Experiment/Demonstration)
- **Template**: “在我们真正[操作/验证]之前，大家不妨先大胆预测一下，如果我们把[参数A]改成[参数B]，[现象/网络]会发生什么变化？”
- **Network Example**: “在我们抓包验证TCP断开连接过程之前，大家不妨先预测一下，既然建立连接需要三次握手，那断开连接是不是也一定是三次挥手呢？”
- **Expected Student Response**: 产生分歧的回答（如“是三次”、“可能是四次”、“看具体情况”），形成认知悬念。
- **Risk**: 学生如果预测完全偏离，教师纠偏时间可能过长；需预设好收拢的“兜底”回应。
- **Difficulty**: High (高)
- **Compatible Strategy**: Cognitive Conflict Questioning, Comparative Questioning

## 2. Follow-up Questioning (启发追问)
- **Recommendation**: ★★★★★
- **Purpose**: 展现教师对学生回答的积极反馈，引导学生从表层现象深入到底层原理。
- **When to Use**: 虚拟学生给出一个表层正确但不全面的回答后，用于深挖知识点。
- **Teaching Stage**: 新知探究 (New Knowledge Exploration), 巩固练习 (Consolidation)
- **Template**: “这位同学回答得非常准确，提到了[学生的回答]。那老师想进一步问问大家，基于这个现象，它的底层机制是怎样的呢？”
- **Network Example**: “A同学说得很好，他观察到路由器是用来连接不同网络的。那老师进一步追问一下，路由器具体是依靠报文里的哪个参数来决定转发路径的呢？”
- **Expected Student Response**: 学生停顿思考，随后给出涉及底层协议、核心参数或报文结构的深层回答。
- **Risk**: 追问过深容易导致冷场或偏题，需提前设计好阶梯式提示或图形辅助。
- **Difficulty**: High (高)
- **Compatible Strategy**: Summarizing Questioning

## 3. Cognitive Conflict Questioning (认知冲突提问)
- **Recommendation**: ★★★★★
- **Purpose**: 刻意制造矛盾或打破常规思维，迅速吸引评委注意力，激发探究欲。
- **When to Use**: 引入重难点概念之前，或者讲完基础理论准备展示特殊情况/进阶概念时。
- **Teaching Stage**: 课堂导入 (Introduction), 难点突破 (Breakthrough of Difficulties)
- **Template**: “刚才我们说[常规结论]。但是大家看大屏幕上这个奇怪的现象：[反常现象]。既然[常规结论]，为什么还会出现这种情况？”
- **Network Example**: “刚才我们测试两台电脑直连是可以Ping通的。现在请看屏幕，我把它们的IP地址改成了192.168.1.10和192.168.2.10，突然就Ping不通了。明明物理网线是好好的，为什么呢？”
- **Expected Student Response**: 感到惊讶，指出可能是逻辑层配置（如子网掩码/网段）或安全策略的问题。
- **Risk**: 铺垫不足时冲突不明显；现象太难时学生无法建立有效猜想，导致变成教师自说自话。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Diagnostic Questioning

## 4. Scenario-based Questioning (情境代入提问)
- **Recommendation**: ★★★★★
- **Purpose**: 将干涩的理论赋予职业应用场景，体现教学与工程实践的结合。
- **When to Use**: 讲解协议抓包、网络排错、设备配置等工程性较强的内容时。
- **Teaching Stage**: 巩固练习 (Consolidation), 难点突破 (Breakthrough of Difficulties)
- **Template**: “假设你是公司的[职业身份]，现在接到了一个需求/故障：[具体场景]。在不动[已有条件]的情况下，你会优先检查哪里？”
- **Network Example**: “假设大家是公司的网络工程师，现在老板的电脑突然打不开网页了，但微信却能正常收发消息。凭借你们的经验，第一时间会怀疑是哪个协议出了问题？”
- **Expected Student Response**: 能将理论知识（如 DNS 解析过程）与实际故障现象精准对应，并给出排查思路。
- **Risk**: 情境设计脱离实际工程标准，或引入了过多不必要的业务细节干扰核心技术点。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Prediction Questioning

## 5. Comparative Questioning (对比观察提问)
- **Recommendation**: ★★★★☆
- **Purpose**: 通过对比差异，凸显核心概念的特征，防止易混淆知识点出错。
- **When to Use**: 介绍具有相似性或升级关系的两个技术（如TCP与UDP、IPv4与IPv6）时。
- **Teaching Stage**: 新知探究 (New Knowledge Exploration)
- **Template**: “请大家对比观察大屏幕上的[图表A]和[图表B]，找一找，它们在[某维度]上最大的区别在哪里？”
- **Network Example**: “请大家认真观察这两张Wireshark抓包图。TCP的通信开始前有明显的三次握手交互，而UDP这边却直接开始传数据。这说明它们在连接机制上有什么最核心的区别？”
- **Expected Student Response**: 能够精准找出两个对比对象的差异点（如“有无握手连接”），并尝试推导其优缺点。
- **Risk**: 对比维度不明显，导致学生找错重点；需要教师有指向性的光标引导或高亮标注。
- **Difficulty**: Low (低)
- **Compatible Strategy**: Summarizing Questioning

## 6. Diagnostic Questioning (诊断探误提问)
- **Recommendation**: ★★★☆☆
- **Purpose**: 暴露学生的潜在误区，通过纠错巩固正确认知。
- **When to Use**: 讲解完易错点或配置难点后，用于检验学习效果。
- **Teaching Stage**: 巩固练习 (Consolidation), 评价反馈 (Evaluation/Feedback)
- **Template**: “有同学/有位初级工程师认为，只要配置了[参数]，就一定能[结果]。大家同意这个说法吗？仔细看看，是不是漏掉了什么关键步骤？”
- **Network Example**: “有同学觉得，只要交换机的VLAN划分好了，两台分属不同VLAN的电脑接上去就能直接通信。大家同意吗？是不是忘记了VLAN‘广播域隔离’的特性？那要怎么才能打破这个隔离？”
- **Expected Student Response**: 敏锐识别出错误所在，并提出修正方案（如“需要配置单臂路由或三层交换”）。
- **Risk**: 若抛出的误区过于冷门或生僻，反而会给原本正确的学生植入错误记忆；应当挑选高频共性错误。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: Follow-up Questioning

## 7. Summarizing Questioning (归纳总结提问)
- **Recommendation**: ★★★☆☆
- **Purpose**: 收束发散的思维，引导学生自主提炼核心结论，体现“以学生为主体”。
- **When to Use**: 某一个小节结束，或者整堂课收尾的总结阶段。
- **Teaching Stage**: 课堂小结 (Summary), 模块收尾 (Module Wrap-up)
- **Template**: “通过刚才的[实验/推导/分析]，哪位同学能尝试用一句话/三个关键词，来总结一下[技术名词]的核心作用？”
- **Network Example**: “通过刚才对OSI七层模型数据封装过程的剖析，哪位同学能尝试用一句话总结一下，传输层和网络层在数据传输中各自承担的最本质的分工是什么？”
- **Expected Student Response**: 能用精炼的专业术语准确概括知识点（如“网络层找主机，传输层找应用”）。
- **Risk**: 学生概括能力不足时容易卡壳，需要教师通过板书关键字或填空式提示进行辅助。
- **Difficulty**: Medium (中)
- **Compatible Strategy**: None

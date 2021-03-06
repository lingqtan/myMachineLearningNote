# 01 绪论

## 1.1 基本概念

- 假设(hypothesis): 学得模型对应的关于数据的某种潜在的规律
- 真实(ground-truth): 潜在的真实规律
- 泛化(generalizaiton): 学得模型适用于新样本的能力
- 分布(distribution): 通常假设样本空间汇中，全体样本服从一个未知的分布，每个样本都是独立从这个分布上采样获得
- 偏好(bias): 在学习过程中，对某种类型假设的偏好，如偏好“尽可能特殊”的模型或偏好“尽可能一般”的模型。
    - 算法的归纳偏好是否与问题本身匹配，大多数时候直接决定了算法能否取得好的性能。
- 奥卡姆剃刀(Occam's razor): 若有多个假设与观察一致，选择最简单的那个
- 没有免费午餐定理(NFL Theorem): 任何学习算法的期望性能相同。
    - 前提：所有问题出现的机会相同/所有问题同等重要。
    - 寓意：脱离具体问题，空谈“什么学习算法最好”毫无意义。

## 1.2 发展历程

### 1.2.1 人工智能发展历程

- 推理期 ['50s - '70s初]
    - 赋予机器逻辑推理能力
    - A. Newell, H. Simon (1975年图灵奖，发明逻辑理论家)
    - 逻辑理论家(Logic Theorist), 通用问题求解程序(General Problem Solving)
        - 逻辑理论家证明了罗素《数学原理》的全部52条定理
- 知识期 ['70s中期开始]
    - 要使机器更具有智能，必须设法使机器拥有知识
    - E. A. Feigenbaum (1994年图灵奖，知识工程之父)
    - 专家系统
    - 知识工程瓶颈：由人来把知识总结出来再教给计算机是相当困难的
- 学习期 ['80s]
    - 机器学习

### 1.2.2 机器学习历史 ['50s初开始]

- 图灵, 关于图灵测试的文章中提到了机器学习的可能(1950年)
- 跳棋程序(A. Samuel, '50s初)
    - Samuel 发明了机器学习一词，定义为“不显式编程地赋予计算机能力的研究领域”
- 连接主义(connectionism)出现 基于神经网络('50s中后期)
    - 感知机(Perceptron, F. Rosenblatt)
    - Adaline(B. Widrow)
- 符号主义(symbolism)出现 基于逻辑表示('60s - '70s)
    - 结构学习系统(P. Winston)
    - 基于逻辑的归纳学习系统(R. S. Michalski)
    - 概念学习系统(E. B. Hunt)
    - 以决策理论为基础的学习技术, 强化学习技术也得到发展
        - 学习机器(N. J. Nilson)
    - 日后的统计学习理论的奠基性结果也是这个时期取得的
- 机器学习成为一个独立的学科领域('80s)

### 1.2.3 "从样例中学习"主流技术演进

- 机器学习被研究最多应用最广的是"从样例中学习"(Michalski, 1983)或称为"归纳学习"(Feigenbaum, 1983)
- 符号主义, "从样例中学习"一大主流 ['80s]
    - 学习结果为明确的概念表示
    - 代表：决策树(decision tree), 基于逻辑的学习
        - 决策树：以信息论为基础，信息熵最小化为目标
        - 基于逻辑的学习，代表：归纳逻辑程序设计(ILP)
            - 使用一阶逻辑(谓词逻辑)进行知识表示，通过逻辑表达式对数据归纳
    - 缺点：由于表示能力太强，导致假设空间太大、复杂度极高，'90s中后期研究陷入低潮
- 连接主义，"从样例中学习"另一大主流 ['90s中期之前]
    - 学习结果为"黑箱"模型
    - 利用神经网络求解"流动推销员问题"(NP问题)取得重大进展(J. J. Hopfield, 1983)
    - BP算法(D. E. Rumelhart, 1986) 被应用最广泛的机器学习算法之一
    - 缺点：试错性——学习过程涉及大量调参，调参过程缺乏理论指导
- 统计学习(statistical learning) ['90s中期]
    - 以统计学习理论为直接支撑，'90s中期成为机器学习的主流
    - 代表：支持向量机(Support Vector Machine), 核方法(kernel methods)
        - "支持向量"概念(V. N. Vapnik, 1963), "VC维"(1968), 结构风险最小化原则(1974)
    - 统计学习与连接主义学习有着密切联系
- 深度学习 [2000s]
    - 卷土重来的连接主义，"很多层"的神经网络
    - 涉及的模型复杂度非常高，缺乏严格的理论基础，但显著降低了机器学习应用者的门槛

## 1.3 应用现状

- 大数据时代的三大关键技术
    - 机器学习(数据分析能力) + 云计算(数据处理能力) + 众包(crowdsourcing, 数据标记能力)
- 数据挖掘(data mining)
    - 数据库领域(数据管理技术) + 机器学习领域(数据分析技术)

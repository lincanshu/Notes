# 一句话概括
- 找了一篇关于联邦学习的激励机制的综述看看，看完个大概就可以主要关注参考文献了（跟区块链相关的，好像都没有发到特别出名的会议期刊）。
- 联邦学习如果没有足够的训练数据和参与者，那么最终模型的性能将会大打折扣，所以这方面的研究着眼于鼓励更多参与者有偿贡献，后面提出说高质量的用户参与的效益远大于一大堆低质量用户。Shapley value用于贡献评估，Stackelberg博弈、auction、契约论用于支付分配，强化学习和区块链作为辅助技术用于节点选择、贡献评估和鲁棒性提升。

# 好奇1：作者指出了哪些未来研究的方向？
- 需要专注于如何通过鼓励更多用户参与，而在保持低开销的条件下，提升模型的表现
- 研究人员应更关注corss-silo FL，虽然我还是不太理解cross-silo的概念，网上有翻译为跨孤井，好比说大组织大公司内部跨部门这种吧。
- 机制设计应该从多维度考量，而不是单维度，另外应该是多目标的
- 前沿技术如图神经网络，应该去寻找新场景（如5G，移动边缘计算）的激励设计的潜在应用。（突然才想到，其实将现有技术投放到新的应用场景也算是一种很重要的创新啊，如果其他人都没有往这个方向去想到）

# 引用
- K. Toyoda and A. Zhang, “Mechanism Design for An Incentive-aware Blockchain-enabled Federated Learning Platform,” in Proc. of IEEE International Conference on Big Data (Big Data), 2019. （提到会每个worker会投票投出前k个模型，并采用智能合约计算前一轮中worker的票数，根据票数得到奖励）
- X. Bao, C. Su, Y. Xiong, W. Huang, and Y. Hu, “FLChain: A Blockchain for Auditable Federated Learning with Trust and Incentive,” in Proc. of IEEE BigCom, 2019. （信任和激励属性）

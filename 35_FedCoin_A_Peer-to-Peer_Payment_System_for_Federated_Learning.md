# 一句话概括
- 开始调研Federated Learning和Block chain结合的一些新的应用，现在是第一篇，重点关注两者结合的设计和实现上的难度。
- 相对于比特币网络需要为了挖矿而求解一些没有任何意义的谜题，作者基于可计算的Shapley Value，提出了带有不可否认和不可纂改属性的激励奖赏给FL参与者的模式，本工作不是为了减少计算复杂度，而是建立了一种新的模式来使分布式计算资源被用于帮助联邦学习系统计算SVs，整个架构设计分为两个网络，联邦学习网络和区块链网络，模型训练系统和支付系统是分开的，支付系统主要承担计算贡献度和计算区块的任务，任务发布者给FL服务器支付，服务器给矿工支付，最后是矿工给客户端支付。
- 据作者的说法，这是目前已知的第一篇将区块链技术引入联邦学习激励模式研究领域。

# 好奇1：中间谈到了SV（Shapley Values）的计算开销是相当大的，那么计算过程是怎样的？
- 现在知道了，这个SV的计算是直接交给矿工去计算的，因为这个计算开销很大，所以依赖区块链强大的算力。

# 好奇2：这个支付体系是怎样的？
- 主要分三部分，TrainPrice是需要支付给FL参与者；ComPrice是需要支付给FL服务器进行模型聚合，模型分发；SapPrice是支付给挖矿的矿工的。

# 引用
- Yu, H., et al.: A fairness-aware incentive scheme for federated learning. In: Proceedings of the 3rd AAAI/ACM Conference on Artificial Intelligence, Ethics, andSociety (AIES-2020) (2020) 目前看到的第一篇有关FL激励机制的顶会论文，大体是说FL参与者必须被公平对待
- Kang, J., Xiong, Z., Niyato, D., Xie, S., Zhang, J.: Incentive mechanism for reliable federated learning: a joint optimization approach to combining reputation and contract theory. IEEE Internet Things J. 6(6), 10700–10714 (2019) 这篇是说将区块链作为辅助技术帮助FL服务器完成节点选择的任务，用以找到可靠和高质量的数据拥有者。
- Ramanan, P., Nakayama, K., Sharma, R.: Baffle: Blockchain based aggregator free federated learning. arXiv preprint arXiv:1909.07452 (2019) 这一篇利用了区块链直接将FL的服务器从FL架构中移除了。
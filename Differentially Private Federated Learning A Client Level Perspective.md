# 一句话概括
- 本文解决的挑战依旧是面对差分攻击下的联邦学习，提出了客户端视角下的差分隐私保护的联邦优化，平衡好隐私损失和模型性能，作者通过实验表明，当参与联邦学习的客户端足够多时，带差分隐私的学习是可行的且有较高的模型精度。
- NIPS 2017是本文接受的会议，没想到已经改了名字，NeurIPS，一度让我以为只是一篇平凡的论文，毕竟是否顶会论文印象还是很不一样的。

# Q1 : 具体的算法细节还没看明白，再琢磨一会。
- 从参考文献看来，属于是较早期将差分隐私引入联邦学习的论文之一，所以在客户端视角来看的话，首次采用高斯机制到中心模型更新是很新颖的做法，而且当客户端数量足够多的时候，对准确率影响不大，

# Q2 : 居然还提供了开源代码！
- https://github.com/SAP-samples/machine-learning-diff-private-federated-learning

# Q3 ： 对于实验也是比较有意思的
- 将MNIST数据集切成碎片，每个客户端拿到两个碎片，这样大多数的客户端只有两个数字，故单一客户端绝不可能训练出高精度地识别全部的十个数字的模型，固定了eplison参数为8，追踪隐私损耗，

# 相关工作
- H. B. McMahan, D. Ramage, K. Talwar, and L. Zhang. Learning differentially private language models without losing accuracy. CoRR, abs/1710.06963, 2017. 与本工作具有相似性
- B. McMahan, E.Moore, D. Ramage, S. Hampson, and B. A. y Arcas. Communication-Efficient Learning of Deep Networks from Decentralized Data. In A. Singh and J. Zhu, editors, Proceedings of the 20th International Conference on Artificial Intelligence and Statistics, volume 54 of Proceedings of Machine Learning Research, pages 1273–1282, Fort Lauderdale, FL, USA, 20–22 Apr 2017. PMLR. 这个就是联邦学习的开山之作了 ，首次提出，值得细品
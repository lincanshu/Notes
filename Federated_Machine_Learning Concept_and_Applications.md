# 一句话概括
- 杨强教授的综述性论文，提出了联邦学习的三个分类就包括了横向联邦学习，纵向联邦学习，联邦迁移学习；
- 横向联邦学习：指的是，多个参与方拥有大量不同的样本ID，但是特征空间却是一致的，举例来说，两个不同的地方银行或机构，它们拥有本地客户所以客户全体交集很小，但是业务模型非常相似，所以数据集的特征空间相同l
- 纵向联邦学习：指的是，多个参与方拥有相同的样本ID，但是特征空间不一致，简单举例，传统银行和电子银行会拥有同一批客户，但是这些客户在不同类别的银行里数据特征维度是不一样的，
- 联邦迁移学习：指的是，两个数据集样本ID不相同的同时，特征空间也不相同，举例来说，位于中国的传统银行和位于美国的电子银行，这些数据只有很少很少的交集，所以会用到迁移学习
- 关于隐私方面，无论是采用差分隐私，K匿名还是多元化，这些方法的本质都是往数据加噪或者泛化方法来模糊敏感属性，使第三方不能够辨别个体因此无法恢复隐私数据，其本质还是准确率和隐私的权衡。

# Q1 : 联邦学习可以看作边缘计算的操作系统？

# Q2 : 

# 相关工作
- 从本文找一些经典论文来看应该是不错的。
- Robin C. Geyer, Tassilo Klein, and Moin Nabi. 2017. Differentially private federated learning: A client level perspective. CoRR abs/1712.07557 (2017). arxiv:1712.07557 http://arxiv.org/abs/1712.07557 这篇已经看过的论文没想到也受到杨强团队的关注，果然是一篇联邦学习+差分隐私的经典论文，值得精读
- Payman Mohassel and Yupeng Zhang. 2017. SecureML: A system for scalable privacy-preserving machine learning. In IEEE Symposium on Security and Privacy. IEEE Computer Society, 19–38. 之前觉得有点奇怪的文章，或者说看不太懂吧，没想到原来是在讲SMC的
- Shiqiang Wang, Tiffany Tuor, Theodoros Salonidis, Kin K. Leung, Christian Makaya, Ting He, and Kevin Chan. 2018. When edge meets learning: Adaptive control for resource-constrained distributed machine learning. CoRR abs/1804.05271 (2018). arxiv:1804.05271 http://arxiv.org/abs/1804.05271. 在给定资源预算下，找到最优的本地更新和全局聚合方案，从而最小化损失函数
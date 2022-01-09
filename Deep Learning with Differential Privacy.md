# 提出的问题
- 大规模的众包数据集在提供给神经网络训练的时候，可能会包含较多敏感信息，所以这里需要能够提供有原则和严格的隐私保证下满足应用程序的需求。

# 解决的方法
- 通过跟踪隐私损失的详细信息，对整体隐私损失做更严格的估计
- 通过介绍新的技术来提升差分隐私训练的计算效率，针对个体训练样本计算梯度，划分子任务到小批次来减少内存占用，

# 解决方案/算法
- 本质上是在SGD随机梯度下降的过程中，多了梯度裁剪和加噪两步


# 引用
@inproceedings{abadi2016deep,
  title={Deep learning with differential privacy},
  author={Abadi, Martin and Chu, Andy and Goodfellow, Ian and McMahan, H Brendan and Mironov, Ilya and Talwar, Kunal and Zhang, Li},
  booktitle={Proceedings of the 2016 ACM SIGSAC conference on computer and communications security},
  pages={308--318},
  year={2016}
}
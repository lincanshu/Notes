# 一句话概括
- 联邦学习的开山之作，首次提出联邦学习的概念，遇到的问题是，面对数据非独立同分布Non-IDD，每个参与训练的客户端拥有数量不同的本地数据，期待的参与FL的客户端远大于实际参与的平均数量，移动设备在通信中处于不利位置如频繁掉线等。
- 作者便提出了著名的联邦平均算法FedAvg，当时的比较对象是FedSGD，可以说达到了相当好的效果，是基于可迭代的模型平均的深度网络联邦学习，

# 解决方案/算法
- 核心思想是将模型参数下发，每个客户端在本地使用SGD算法和本地数据进行训练，最后将模型参数汇总到服务器，服务器执行模型参数平均

# 引用
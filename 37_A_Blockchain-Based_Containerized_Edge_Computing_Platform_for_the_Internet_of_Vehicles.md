# 一句话概括
- 这篇是子腾师兄的IOT论文，也还是中科院一区期刊，着重关注点为区块链在该工作中发挥的作用，另外边缘计算跟车联网的结合很好理解，车辆有计算任务需要满足低延迟的条件，所以采用边缘服务器实现快速计算（一般涉及边缘计算就是使延迟最小化了）
- CUTE是一个容器化和基于区块链的边缘计算平台，提供给车联网用户以低延迟的计算服务，车辆通过通用接口提交计算任务，适当的服务器调度其对应的容器来最小化计算延迟，而区块链是用来提高安全性的，实验结果主要表明作者设计的调度策略优于传统的算法。
- 刚跟导师聊完，发现这里的Paper只是说为了赶一个区块链的期刊会议，只是用来讲故事而已，没有太大的价值。。。

# 好奇1：作者说区块链用来提升边缘计算的网络安全性，具体的呢？
- 区块链不需要中心化验证就可以实现分布式边缘节点的共识，所以非常适合分布式边缘计算架构，在这里是可以通过投票来验证交易从而提高可靠性。
- 哦我悟了，车辆通过统一接口提交计算任务，控制器调度对应的边缘服务器来计算并返回结果，（这个交易过程里，车辆可能需要支付相应费用，而平台方提供算力资源），利用区块链不可纂改性记录下来从而保证可靠性。

# 引用
# 一句话概括
- 本文的应用场景面向车联网，使用基于本地差分隐私的联邦学习来训练机器学习模型，采用了众包的方式运作，各个车主在使用app时可能会暴露用户位置信息、交通信息、机动车信息等，主要解决的问题是降低隐私泄露的威胁以及减少通信开销，后面提出了四种不同的LDP机制来对训练后的模型参数进行扰动。
- 跟我之前想做的事情比较相似，不过我的应用场景主要是智慧工地，可能需要跟导师沟通下。

# Q1 : 算法核心？
- 其实就是在联邦学习的基础上，在客户端上传更新梯度之前，添加LDP噪声后再上传服务器，使得攻击者无法反推原始数据。

# Q2 : 论文的亮点？
- 设计出针对不同大小隐私预算的四种LDP机制，使其最优
- 使连续型输出离散化，从而减少通信开销

# 相关工作
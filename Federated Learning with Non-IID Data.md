# 一句话概括
- 联邦学习在本地数据非独立同分布的情况下，如何处理这个统计学上的挑战，作者提出了一种数据共享的策略data-sharing strategy来提高算法在数据非独立同分布下的训练。
- 看下来作者的思路是，需要在所有的边缘设备中共享一小部分云端制造的全局数据，从而提高准确度，另外这个策略只在模型初始化的时候执行一次，所以不会带来太大的通信开销，看起来并不是一篇特别优秀的paper。

# Q1 : 其实是没有搞清楚，非独立同分布为啥影响了联邦学习模型？
- 可能也不需要太纠结，这里无非是作者通过实验证明了确实降低了精确度。

# Q2 : 

# 相关工作
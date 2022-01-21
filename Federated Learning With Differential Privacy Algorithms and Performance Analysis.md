# 提出的问题
- 联邦学习中，仍可能通过分析从客户端上传的参数，使得私有信息被泄露。

# 解决的方法
- 提出了一个模型聚合前加噪的NbAFL模式，并证明其适应差分隐私
- 提出NbAFL在训练过程中的损失函数的一个收敛界限，并发现了，收敛性能与隐私保护水平的trade-off，增加FL中的客户端数量N能够提高收敛性能，在给定隐私保护水平下存在最优的最大聚合次数
- 提出了N个客户端参与的联邦学习的K客户端随机调度策略，并找出最优的K值来实现固定隐私水平的最有收敛性能

# 解决方案/算法
- 本质上是在客户端上传训练参数之前加噪，且服务端下发加噪的全局参数


# 引用
@ARTICLE{9069945,  author={Wei, Kang and Li, Jun and Ding, Ming and Ma, Chuan and Yang, Howard H. and Farokhi, Farhad and Jin, Shi and Quek, Tony Q. S. and Poor, H. Vincent},  journal={IEEE Transactions on Information Forensics and Security},   title={Federated Learning With Differential Privacy: Algorithms and Performance Analysis},   year={2020},  volume={15},  number={},  pages={3454-3469},  doi={10.1109/TIFS.2020.2988575}}
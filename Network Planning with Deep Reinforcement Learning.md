# 提出的问题
- 具体问题，网络规划问题，这个问题一般求解都是采用整数线性规划，针对这个问题没有充足的背景知识进行理解，大致意思是现代骨干网需要满足用户需求、服务和交通模式

# 解决的方法
- 提出了NeuroPlan，用来解决网络规划问题的深度学习方法
- 基于节点链路转换和图神经网络，设计了特定领域的技术，并利用混合了深度强化学习和整数线性规划来找到最优解
- 实现了NeuroPlan原型，提供了开源代码，相对于手调启发式降低了17%的消耗
- https://github.com/netx-repo/neuroplan

# 解决方案/算法
- 求解这个问题分两步，第一步是用deep RL来大规模剪枝，第二步是用ILP来快速找到最优解


# 引用
@inproceedings{10.1145/3452296.3472902,
author = {Zhu, Hang and Gupta, Varun and Ahuja, Satyajeet Singh and Tian, Yuandong and Zhang, Ying and Jin, Xin},
title = {Network Planning with Deep Reinforcement Learning},
year = {2021},
isbn = {9781450383837},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3452296.3472902},
doi = {10.1145/3452296.3472902},
abstract = {Network planning is critical to the performance, reliability and cost of web services. This problem is typically formulated as an Integer Linear Programming (ILP) problem. Today's practice relies on hand-tuned heuristics from human experts to address the scalability challenge of ILP solvers.In this paper, we propose NeuroPlan, a deep reinforcement learning (RL) approach to solve the network planning problem. This problem involves multi-step decision making and cost minimization, which can be naturally cast as a deep RL problem. We develop two important domain-specific techniques. First, we use a graph neural network (GNN) and a novel domain-specific node-link transformation for state encoding, in order to handle the dynamic nature of the evolving network topology during planning decision making. Second, we leverage a two-stage hybrid approach that first uses deep RL to prune the search space and then uses an ILP solver to find the optimal solution. This approach resembles today's practice, but avoids human experts with an RL agent in the first stage. Evaluation on real topologies and setups from large production networks demonstrates that NeuroPlan scales to large topologies beyond the capability of ILP solvers, and reduces the cost by up to 17% compared to hand-tuned heuristics.},
booktitle = {Proceedings of the 2021 ACM SIGCOMM 2021 Conference},
pages = {258–271},
numpages = {14},
keywords = {network planning, reinforcement learning, graph neural network},
location = {Virtual Event, USA},
series = {SIGCOMM '21}
}
# 一句话概括
- 面对联邦SGD中的隐私泄露问题，作者提出了FedSel算法，其中就包括了维度选择和值扰动，利用TopK的方式来选择数据中k个贡献最大的维度来进行值扰动，这里的挑战是如何设计出在LDP下的联邦SGD的更好的选择策略。
- 我的简单理解就是精准扰动，把数据扰动控制到一部分参数上，从而降低加噪对整个模型的影响。

# Q1 : 

# Q2 : 

# 相关工作
- Yang, Q., Liu, Y., Chen, T., Tong, Y.: Federated machine learning: concept and applications. ACM Trans. Intell. Syst. Technol. (TIST) 10(2), 1–19 (2019) 杨强教授的论文，我觉得可以看看

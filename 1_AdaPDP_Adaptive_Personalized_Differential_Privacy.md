# 一句话概括
- 通常用户把自己的数据贡献给数据集以供使用，现存的问题是，有些用户被过度保护，同时框架的设计没有明确地包含模型可用性，所以作者提出了具有自适应功能的定制化差分隐私框架AdaPDP，想法不错，这个确实是他们工作的亮点，针对不同用户对隐私的敏感度不同这一情况进行设计，达到一种私人定制的效果，自适应地选择潜在的加噪算法，目标是最大化模型可用性，并基于查询函数的类型，数据分布和隐私设置来计算对应的参数。
- 看下来总体是基于查询函数对后续隐私操作进行优化，跟机器学习关系不是很大，还是在围绕着隐私机制如何设计展开的工作，只能说没有太大的参考性。

# Q1： 对模型的细节有点兴趣。
- 每个用户提交自己的隐私数据和隐私预算给服务提供商，消费者提交查询需求，服务提供商返回查询结果，由于查询结果已经被添加扰动，所以不会暴露用户的敏感信息。
- 首先把敏感数据集、用户的隐私预算、查询函数作为输入，得到基于查询函数的合适的噪声生成算法，接着计算出参数最优值用于效用感知采样机制，最后执行多轮采样来最大化数据利用率。

# 引用
- C. Dwork, F. McSherry, K. Nissim, and A. Smith, “Calibrating noise to sensitivity in private data analysis,” in Springer TCC, 2006. 这篇就是介绍Laplace机制的经典论文
- F. McSherry and K. Talwar, “Mechanism design via differential privacy,” in IEEE FOCS, 2007. 这篇是介绍指数机制的经典论文
- Z. Jorgensen, T. Yu, and G. Cormode, “Conservative or liberal? personalized differential privacy,” in IEEE ICDE, 2015. 这篇讲解定制化差分隐私机制
- F. Li, H. Li, B. Niu, and J. Chen, “Privacy computing: Concept, computing framework, and future development trends,” Engineering, vol. 5, no. 6, pp. 1179–1192, 2019. 作者说是按照这篇paper来设计评估AdaPDP
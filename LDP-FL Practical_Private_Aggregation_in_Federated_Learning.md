# 一句话概括
- 本文提出了LDP-FL一个新的本地差分隐私机制，主要创新点就是对算法进行了稍微改造，除了平时的添加数据扰动外，在客户端还多了一步参数洗牌Parameter Shuffling，这个参数洗牌似乎是全篇最大的亮点？虽然在我看来也不是非常厉害的操作。

# Q1 : Parameter Shuffling具体是如何操作的？
- 说实话挺简单的，就是将不同模型的参数进行打乱，比如M1里的部分参数放在M2，M3里面的相同位置，从而打乱顺序，但我比较质疑它的可行性。

# Q2 : 

# 相关工作
- 文献参考居然都没有标号的，太离谱了，从这一点看真不是什么好Paper
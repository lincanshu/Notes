# 提出的问题
- 带宽测试测量对新型的网络感知内容交付应用非常重要，然而今天的带宽测量服务又慢又开销巨大，作者认为造成这些低效率的原因是处理噪声所产生的时空冗余

# 解决的方法
- FastBTS的关键思想是通过一种新颖的统计采样框架来适应和利用噪声，从而消除了长时间测试持续时间和耗尽资源使用来抑制噪声影响的需要,

# 解决方案/算法
- EBP弹性带宽探测机制，可根据与当前估计带宽的偏差来调整传输层数据探测速率
- CIS关键区间采样算法，实现了模糊拒绝采样的接受拒绝函数
- DSS数据驱动的服务器选择，这个好理解，通过数据驱动模型来选择最高带宽的服务器，通过研究发现现有的PING延迟最低的服务器选择算法是低效的，原因是延迟和可用带宽并不存在高度相关，测试服务器包含{延迟、吞吐量}的数据模型，可以基于期待的吞吐量值进行排名选出对应的服务器
- ANH自适应多宿主机制，用于在需要的时候对不同的测试服务器建立多个并行的连接

# 引用
@inproceedings{DBLP:conf/nsdi/YangW0LQGMX21,
  author    = {Xinlei Yang and
               Xianlong Wang and
               Zhenhua Li and
               Yunhao Liu and
               Feng Qian and
               Liangyi Gong and
               Rui Miao and
               Tianyin Xu},
  editor    = {James Mickens and
               Renata Teixeira},
  title     = {Fast and Light Bandwidth Testing for Internet Users},
  booktitle = {18th {USENIX} Symposium on Networked Systems Design and Implementation,
               {NSDI} 2021, April 12-14, 2021},
  pages     = {1011--1026},
  publisher = {{USENIX} Association},
  year      = {2021},
  url       = {https://www.usenix.org/conference/nsdi21/presentation/yang-xinlei},
  timestamp = {Thu, 12 Aug 2021 18:19:16 +0200},
  biburl    = {https://dblp.org/rec/conf/nsdi/YangW0LQGMX21.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
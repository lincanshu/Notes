# 提出的问题
- 网络流量测试是成功网络运营的核心，尤其是如今的超大规模网络，现存工作的主要问题是还没有同时实现以下三个标准，完全可见性即能够为所有流获取所需的每跳流级别的信息；在计算、内存和带宽方面的低开销；鲁棒性即部分网络故障时仍能正常运作。
- 延迟的评估，丢包的检测，异常抖动的检测，跟踪转发路径

# 解决的方法
- 提出了小程序并设计了一个轻量级的带内遥测系统。
- 设计 SuMax 草图以支持常见且更重要的高精度测量任务。
- 设计了一种增量重建算法来实现鲁棒性和容错性。
- 实现了一个 LightGuardian 原型并将其开源。
- https://github.com/Light-Guardian/LightGuardian

# 解决方案/算法
- 主要创新是一个（小的）恒定大小的数据结构，称为skettlelet，它可以嵌入到数据包header中。具体来说，设计了一个新颖的SuMax草图来准确捕获流量级信息。SuMax 可以分为sketchlets，这些sketchlets通过将数据包传递到最终主机进行聚合、重建和分析而带内传输。

# 引用
@inproceedings{DBLP:conf/nsdi/ZhaoYLYCLZWWWZ21,
  author    = {Yikai Zhao and
               Kaicheng Yang and
               Zirui Liu and
               Tong Yang and
               Li Chen and
               Shiyi Liu and
               Naiqian Zheng and
               Ruixin Wang and
               Hanbo Wu and
               Yi Wang and
               Nicholas Zhang},
  editor    = {James Mickens and
               Renata Teixeira},
  title     = {LightGuardian: {A} Full-Visibility, Lightweight, In-band Telemetry
               System Using Sketchlets},
  booktitle = {18th {USENIX} Symposium on Networked Systems Design and Implementation,
               {NSDI} 2021, April 12-14, 2021},
  pages     = {991--1010},
  publisher = {{USENIX} Association},
  year      = {2021},
  url       = {https://www.usenix.org/conference/nsdi21/presentation/zhao},
  timestamp = {Thu, 12 Aug 2021 18:19:16 +0200},
  biburl    = {https://dblp.org/rec/conf/nsdi/ZhaoYLYCLZWWWZ21.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
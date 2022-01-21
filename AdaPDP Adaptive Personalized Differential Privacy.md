# 提出的问题
- 通常用户把自己的数据贡献给数据集以供使用的时候，会有不同隐私需求。现有的PDP机制可以在不暴露个体隐私下来呈现整个数据集的统计信息。
- 问题在于，这些现有机制会造成查询结果的低精确度，进而导致较差的数据利用率。
- 这里主要的trade-off是隐私预算和数据利用率，挑战就在于如何设计PDP机制，在不影响所有用户非统一的隐私需求不，减少预算的浪费

# 解决的方法
- 提出了自适应私有差分隐私框架AdaPDP，在不同情景下最大化数据利用率，其自适应地选择潜在的加噪算法，并基于查询函数的类型，数据分布和隐私设置来计算对应的参数。
- 另外，AdaPDP执行了多轮效用感知采样来满足用户不同的隐私需求，重用浪费的预算来增加数据利用率
- 严格地证明了多轮效用感知采样机制

# 解决方案/算法


# 引用
@INPROCEEDINGS{9488825,  author={Niu, Ben and Chen, Yahong and Wang, Boyang and Wang, Zhibo and Li, Fenghua and Cao, Jin},  booktitle={IEEE INFOCOM 2022 - IEEE Conference on Computer Communications},   title={AdaPDP: Adaptive Personalized Differential Privacy},   year={2021},  volume={},  number={},  pages={1-10},  doi={10.1109/INFOCOM42981.2021.9488825}}
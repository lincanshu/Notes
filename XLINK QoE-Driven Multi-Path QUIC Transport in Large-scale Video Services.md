# 提出的问题
- 如何提高视频传输的效率，如何给终端用户提供更高的用户体验质量QoE，现有方法未能足够快地使调度适应底层路径带宽的变化。
- 这个课题还是比较有意思的，跟我的深信服项目有点像，不过这里主要面向视频数据来提高QoE
- 将多路径QUIC带入到大规模视频服务是否有价值？

# 解决的方法
- 基于淘宝短视频的业务需求进行设计，提出了XLINK框架来解决，XLINK被设计为一个轻量级的端到端的多路径QUIC拓展并部署到移动应用和边缘服务器上
- 实现传输层和应用层级别的优先级注入，传统的数据包重注入可以实现，将慢链路丢失的数据包重新放到快链路发送，从而降低时间消耗；QUIC流有两种的情况下，基于优先级是指会将丢失数据包放到未发送的流之前，达到快速恢复的效果
- 建立多路径连接，框架图中移动终端分别同时通过LTE和WIFI建立连接，数据包会进行拆分并放到不同的路径传输，
- 双阈值控制算法，

# 实现的效果
- 生产环境下的第一个大规模的多路径QUIC视频服务
- improvement主要包括三个方面：视频块请求完成时间，第一视频帧延迟，以 2.1% 的冗余流量为代价来提高重新缓冲率
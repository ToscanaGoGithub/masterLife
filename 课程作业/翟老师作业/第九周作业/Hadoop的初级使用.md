-File /input/data.txt._COPYING_ could only be replicated to 0 nodes instead of minReplication (=1)
    结点未全部启动，需要重新配置一下
    参考： https://blog.csdn.net/hewsonchen/article/details/89436021

- 通过hadoop自带的demo运行单词统计
    -参考：https://blog.51cto.com/13153175/1951631
    辅助验证运行hadoop 2.7.4自带demo程序验证环境 https://www.cnblogs.com/xiaochangwei/p/7466938.html

-安装模式 hadoop mkdir: Cannot create directory /usr. Name node is in safe mode.
    离开安全模式 bin/hadoop  dfsadmin -safemode leave

 -安装教程  docker环境下搭建hadoop集群(ubuntu16.04 LTS系统） https://blog.csdn.net/weixin_42051109/article/details/82744993

 -[Hadoop踩坑]MapReduce的一个小实验（wordcount） https://www.imooc.com/article/36490
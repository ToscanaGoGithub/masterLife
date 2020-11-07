
使用镜像安装Hadoop大致流程：
    拉取阿里镜像
    查看镜像
    创建Hadoop容器
        创建master结点
        创建slave1和slave2
        查看容器 docker ps -s
    进入容器 docker exec -it master bash
    配置ssh生成密钥，配置所有的结点 ssh-keygen -t rsa
    为每个结点配置ip地址，vim /etc/hosts进行配置，使用ssh mater进行测试
    配置Hadoop
运行Hadoop
    配置slaves
    在master上格式化namenode
    在master启动集群 cd /opt/tools/hadoop/sbin/  ./start-all.sh
    jps查看进程，表明已经安启动成功


连接ssh失败
开启22端口
安装相关命令行的包yum install firewalld 

参考：使用docker安装分布式hadoop（阿里hadoop镜像） https://blog.csdn.net/k393393/article/details/91410409
完整版
1/下载镜像，也就是docker pull
2/dockers image 察看镜像是否下载成功
3/使用镜像创建容器，master slave1 slave2
4/创建master docker run


查看Docker容器的信息
    -创建docker docker run --name tomcat001 -idt tomcat
    -查看是否成功 docker ps
获取信息常用的方式有如下三种：
    进入容器内部获取信息；
    执行docker exec命令；
    执行docker inspect -f命令（推荐方式）；


参考： https://blog.csdn.net/weixin_42051109/article/details/82744993 docker环境下搭建hadoop集群(ubuntu16.04 LTS系统）
https://blog.csdn.net/boling_cavalry/article/details/80215214 查看Docker容器的信息
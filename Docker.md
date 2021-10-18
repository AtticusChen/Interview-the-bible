#### 1.什么是Docker
    Docker是一个容器化平台
    它以容器的形式将您的应用程序及其所有依赖项打包在一起，
    以确保您的应用程序在任何环境中无缝运行。
#### 2.Docker与虚拟机有何不同
    1.容器不需要引导操作系统内核，因此在创建容器的时候时间特别短。
    2.容器的虚拟化为主机增加了几乎没有的开销，因此容器的虚拟化更接近本机性能
    3.容易不需要其他软件
    4.主机与容器共享调度程序，节省了其他额外资源需求。
#### 3.什么是Docker镜像
    Docker镜像是Docker容器的源代码，Docker镜像用于创建容器。使用build命令创建镜像。
#### 4.Docker容器有几种状态
    四种状态：运行、已暂停、重新启动、已退出。
#### 5.DockerFile中最常见的指定是什么?
        指令      备注
        FROM	指定基础镜像
        LABEL	功能为镜像指定标签
        RUN	    运行指定命令
        CMD	    容器启动时要运行的命令
#### 6.DockerFile中的命令copy和add命令有什么区别？
    COPY和ADD的区别时COPY的SRC只能是本地文件，其他用法一致。
#### 7.Docker的常用命令？
    docker pull         下拉指定镜像
    docker push         将镜像推送远程仓库
    docker rm           删除容器
    docker rmi          删除镜像
    docker images       列出所有镜像
    docker ps           列出所以容器
#### 8.容器与主机之间的数据拷贝命令？
    Docker cp命令用于容器与主机之间的数据拷贝
    主机到容器：docker cp /www 96f7f14e99ab:/www/
    容器到主机：docker cp 96f7f14e99ab:/www /tmp
#### 9.有什么方法确定一个 Docker 容器运行状态
    docker ps -a
    这将列表形式输出运行在主机上的所有 Docker 容器及其运行状态。
    从这个列表中很容易找到 想要的容器及其运行状态。
#### 10.如何停止所有正在运行的容器？
    使用docker kill $(sudo docker ps -q)
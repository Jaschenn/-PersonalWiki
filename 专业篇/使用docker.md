# 使用 Docker 安装 Hadoop 集群
> Hadoop生态是大数据领域几乎绕不过去的东西，但是配置文件较为复杂。配置起来繁琐复杂容易出错误，使用docker可以加快这一过程。

Docker安装配置不再赘述，可以使用 HomeBrew 或者是在官网下载安装都可以。

* docker使用cp复制容器与宿主机之间的文件
首先使用```docker ps ```找到目前正在运行的容器，目的是找到id

![忽略映射的一堆端口...](https://tva1.sinaimg.cn/large/006y8mN6ly1g6mclqzyh8j325808gjs4.jpg)

那个Container ID就是我们需要找的ID。

# 使用docker cp 复制文件

```bash
docker cp [OPTIONS] SRC_PATH|- CONTAINER:DEST_PATH
```

例如：
```
docker cp /root/test.txt ecef8319d2c8:/root/
```
将本机 root/test.txt 文件复制到ecef8319d2c8容器中的/root/中。


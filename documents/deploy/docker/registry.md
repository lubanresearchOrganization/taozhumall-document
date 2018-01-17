- 安装命令
```
docker pull registry
docker run -d -p 5000:5000 -v /opt/data/registry:/var/lib/registry registry
```
- 客户端连接registry的时候需要
添加一个文件/etc/docker/daemon.json，内容如下
```
{
    "insecure-registries" : [ "registry.lubanresearch.com:5000" ]
}
```

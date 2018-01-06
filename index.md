# lubanmall
## 设计
### [项目设计](documents/design/index.md)
### [数据库表设计](documents/design/dbdesign.md)
### 技术选型
#### spring cloud
#### axon https://www.zybuluo.com/iamfox/note/93864 http://www.axonframework.org
## 部署
分两台机器
### 部署机 4G内存
###### [potainer启动](documents/deploy/docker/potainer.md)
###### jenkins，为了加快构建，配置了lubanresearch.com的host
###### service
###### ui
### 前端机 2G内存
###### nginxserver
### 数据库
#### [mysql安装](documents/deploy/db/mysql.md)
### docker
#### [docker安装](documents/deploy/docker/docker.md)
#### [docker基础镜像](documents/deploy/docker/baseImage.md)
#### [registry安装](documents/deploy/docker/registry.md)
#### [jenkins安装](documents/deploy/docker/jenkins.md)
#### [maven构建](documents/deploy/docker/maven.md)
### web配置
#### [端口配置](documents/deploy/web/ports.md)
#### [nginx](documents/deploy/web/nginx.md)
#### [测试页面](0.1_mindmap.html)




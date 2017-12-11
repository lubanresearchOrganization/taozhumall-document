jenkins

拉取镜像
docker pull jenkins:2.60.3
创建目录
mkdir /opt/data/jenkins_home
chmod 777 /opt/data/jenkins_home

启动jenkins
docker run -d -u root -p 5701:8080 -p 5702:50000 --env JAVA_OPTS="-Xmx256m" -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/usr/bin/docker:ro -v /usr/lib64/libltdl.so.7:/usr/lib/x86_64-linux-gnu/libltdl.so.7  -v /opt/data/jenkins_home:/var/jenkins_home jenkins:2.60.3
到/opt/data/jenkins_home/secrets目录下，查看密码
cat initialAdminPassword
用这个密码登录jeckins

设置密码用户均为admin
安装推荐的插件，另外再安装maven插件
启动命令
```
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v /opt/portainer:/potainerdata portainer/portainer
```
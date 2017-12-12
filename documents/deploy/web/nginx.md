nginx使用对应项目里面的nginxserver打包生成的镜像,由于sso里面用到了servlet api获取
server name 的方法，在 nginx代理的情况下，在每个server添加了如下配置

      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Real-PORT $remote_port;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
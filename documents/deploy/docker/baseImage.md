关于基础镜像，主要有以下几点考虑
- 减少每次代码更新，构建的时候docker上传到registry的大小,所以
把一些常用的jar包放到一个基础镜像里面
- 因为需要在部署的时候让java应用自动适应外部设置给docker容器的
内存大小，市面上有三种方法，
   
   - 一是利用jdk9的原生支持:
       ```
       -XX:+UnlockExperimentalVMOptions
       -XX:+UseCGroupMemoryLimitForHeap
        ```
  - 二是利用在镜像里面获取当前cgroup的大小，计算出jvm可以利用的最大值，然后跑启动参数的
  时候设置进去;
  
  - 三是在基础镜像里面设置好(实际操作也是用得这种办法)
    新建两个基础镜像，一个ui,一个service的

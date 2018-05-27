1. intellij idea启动

   1. 取消弹出的tips的勾
   2. 取消代码的自动分析,比如sonarlint等代码审查的自动触发分析(这项不一定做)
   3. 去除不必要的插件
   4. 调整虚拟机参数，设置好内存之类的,-Xms和-Xmx工具内存可以设置小一点
       ```
       -ea
       -server
       -Xverify:none
       -Xms2000m
       -Xmx4000m
       -XX:MaxPermSize=1000m
       -XX:NewRatio=4
       -Xss1m
       -XX:+UseParallelGC
       -XX:ParallelGCThreads=2
       -XX:+UseAdaptiveSizePolicy
       -XX:+UseFastAccessorMethods
       -XX:+UseThreadPriorities
       -XX:+AggressiveOpts
       -Dsun.awt.keepWorkingSetOnMinimize=true
       -Djava.awt.im.style=on-the-spot
       -XX:SoftRefLRUPolicyMSPerMB=50
       -Dsun.io.useCanonCaches=false
       -Djava.net.preferIPv4Stack=true
       -Djsse.enableSNIExtension=false
       -XX:+HeapDumpOnOutOfMemoryError
       -XX:-OmitStackTraceInFastThrow
       -Dawt.useSystemAAFontSettings=lcd
       -Dsun.java2d.renderer=sun.java2d.marlin.MarlinRenderingEngine
       -XX:ReservedCodeCacheSize=240m
       -XX:+AlwaysPreTouch
       -XX:+TieredCompilation
       -XX:+UseCompressedOops
       -XX:+CMSParallelRemarkEnabled
       -XX:ConcGCThreads=4
       ```            
   5. ide和jvm以及代码、maven库都确保在电脑上较快的盘上面比如ssd上面
2. 关闭杀毒软件
3. 切换窗口命令,减少同时存在的窗口数
4. 最好减少输入法切换,用英文写注释
6. 减少断点，去除方法名上面的断点
7. 程序启动
    在Before Launch下面的make去掉，执行File->Invalidate Caches /Restart 
8. 代码编译
    勾中comiple independent modules in parallel
9. 代码重新热部署
    安装jrebel
10. 代码检查
    取消代码拼写检查(可选),Settings->Inspections > Spelling > Typo
11. 调试
12. git工具
13. maven依赖冲突解决
14. 统一编码格式：
    File -> Settings -> Editor -> File Encodings -> 设置 IDE Encoding、Project Encoding、Defalut encoding for properties files
    勾选 Transparent native -to-ascii conversion
15. 过滤的文件类型及目录：
    File -> Settings -> Editor -> File Types -> Ignore files and folders -> 添加 .iml;.idea;.classpath;.project;*.settings;target;
16. 关闭自动检测新版本更新：
    File -> Settings -> Appearance & Behavior -> System Settings -> Updates -> 去掉 Automatically check updates for
17. 代码编辑
    快捷键，如果熟悉eclipse,可以修改成eclipse的快捷键




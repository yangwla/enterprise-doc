## 全服务器还原

### 还原规则的配置和启动 {#-0}

通过控制机管理界面，进入全服务器保护-&gt;全服务器还原界面：

![](/assets/V6.1.2018122609.png)

点击“新建”按钮，进入全服务器还原规则定义界面：

![](/assets/V6.136468.png)

* “名称“：全服务器还原的名称，便于管理
* “全备服务器“：全服务器备份的灾备机
* “数据存放目录“：灾备机上存放需要还原的数据的目录
* “还原客户端“：需要将数据恢复到这台机器
* “同步项“：用户自定义选择要同步的磁盘，比如：C: ,E:\,F:\;
* “全备服务器目录“：灾备机上需要还原的目录
* “还原客户端目录“：还原到客户机上的目录

网络设置页面如下：

![](/assets/V6.137295.png)

* “将工作机的网络配置同步到灾备机”：用户可自定义选择，当主机含有多个网卡时，可以选择同步其中的一些网卡，或者是全部同步；
* “网卡映射”：用户自定义，主机和备机的网络配置的对应关系；

![](/assets/V6.137388.png)

还原设置页面如下：

![](/assets/V6.137395.png)

* “完成系统和数据同步之后，自动关闭工作机和切换到灾备机”: 暂时不提供该功能。

其他设置参见：
* [复制规则高级属性](coopy_cdp/advance_settings.md)


提交之后，i2自动检查主机和备机是否满足服务器还原的条件，只有以下条件检查通过才可以提交任务：

![](/assets/V6.033331.png)

检查通过，提交任务之后，回到任务监控界面：

![](/assets/V6.1.2018122609.png)

### 任务监控和全服务器还原 {#-1}

全服务器还原任务首先会将数据一次性还原到指定机器上，此过程称为镜像，镜像时间的长短取决于初始数据的大小、网络的速度以及镜像的算法，在状态栏会显示镜像的进度。

![](/assets/V6.1.2018122609.png)

全服务器还原任务对应的操作如下，第一排从左到右依次;

* “启动”：启动任务;
* “停止”：停止任务;
* “删除”：删除任务；
* “查看”：查看任务；
* “查看数据流量”：查看实时数据流量图
* “查看日志”：查看日志
* “从源端迁移到目标端”，当规则状态为迁移就绪时，用户可以点击该图标实现从源端到目标端的迁移。
* “重启目标端系统“：只有状态为重启就绪时才可以点击

当镜像完成后，规则进入’迁移就绪’状态，如下：
![](/assets/V6.1.2018122610.png)

点击“从源端迁移到目标端”：

![](/assets/V6.1.2018122611.png)


规则状态变为“重启就绪”：

![](/assets/V6.1.2018122612.png)


点击“重启目标端系统”，如下：

![](/assets/V6.1.2018122613.png)

点击“确定”，如下：


![](/assets/V6.1.2018122614.png)

等规则状态变为“迁移完成”，即整个全服务器还原过程完成：

![](/assets/V6.1.2018122615.png)

综上所述，全服务器还原任务的状态转换过程如下：

![](/assets/V6.033779.png)


备份管理-&gt;备份-&gt;基本设置

*   “备份名称”：备份规则的名字可按照自己的习惯填写
*   “工作机”：系统自动列出该用户创建的所有工作机节点和混合节点
*   “灾备机“：系统自动列出所有灾备机节点和混合节点
*   “源类型”：源类型分为四类 文件，块设备，oracle，mssql server
*   “目标类型”：文件，raw数据

源类型与目标类型的对应关系：文件-&gt;文件，文件-&gt;raw数据，块设备-&gt;文件，块设备-&gt;raw数据，oracle-&gt;文件，mssql server-&gt;文件

**选择 块设备-&gt;文件，或块设备-&gt;raw数据**即块备份

![说明: 1](/assets/V7.000013.png)

*   “工作机源目录和文件“：在linux或者windows 中可通过页面添加块设备，添加页面如下：

![说明: 1](/assets/V7.200001.png)

![说明: 1](/assets/V7.038101.png)

*   “灾备机目标路径”：工作机需要保护的文件或者目录将要备份到此目录下
*   “删除策略”：删除策略及删除该规则时删除目标路径下备份的数据，在默认情况下此策略没有被选中如果有此需求建立规则时可以自行勾选
*   “块备份”：勾选“直接拷贝”表示备份到灾备机后以文件的形式存在，不勾选表示以目录的形式存在

备份管理-&gt;备份-&gt;备份设置

![说明: 1](/assets/V7.038591.png)

以为参数的意义同复制规则的高级选项原理相同故在此不做过多解释

备份管理-&gt;备份-&gt;压缩加密

![说明: 1](/assets/V7.038599.png)

以为参数的意义同复制规则的高级选项原理相同故在此不做过多解释

备份管理-&gt;备份-&gt;备份策略

![说明: 1](/assets/V7.000002.png)

*   立即执行：提交规则后立即做一次备份
*   一次性任务：提交规则后在指定的时间开始做一次备份
*   周期性任务：提交规则后根据备份策略指定的具体时间做周期性备份，比如每天某时某刻、每周某时某刻、每月某时某刻做周期性备份
*   开始时间：开始时间即备份的开始时间请按需求自己手动选择
*   数据保留期限：备份到灾备机的数据所要保留的期限根据备份策略中的策略类型而分为多少天、多少周、多少月。
*   添加策略：备份策略通过此按钮来添加

**添加备份策略**

点击“添加策略”按钮会出现添加备份策略的弹框，根据策略类型分为“每天” “每周” “每月”

*   按天方式循环运行可以在每天的指定时间点自动运行备份任务，如图

![说明: 1](/assets/V7.000006.png)

*   按周循环的方式支持指定一个星期的某几天的指定时间点自动运行备份任务，如图

![说明: 1](/assets/V7.000007.png)

*   按月循环的方式支持指定月中某几天的指定时间点自动运行备份任务，如图

![说明: 1](/assets/V7.000008.png)

*   备份方式：分为全备、增量、差异等备份方式，根据实际需求选择

![说明: 1](/assets/V7.000009.png)


下面一每天为例添加备份策略，例如现在需要在每天12：00和00:00各进行一次备份，备份方式为全备，则选择备份方式为“全备”，策略类型为“每天”，添加运行时间12:00,00:00，如图
点击“确定”，添加12:00

![说明: 1](/assets/V7.000010.png)

点击“确定”，添加一条备份策略

![说明: 1](/assets/V7.000011.png)

如图，添加完成一条备份策略

![说明: 1](/assets/V7.000012.png)

备份策略可添加多条，请根据实际需求来添加

* [返回备份页](backup.md)
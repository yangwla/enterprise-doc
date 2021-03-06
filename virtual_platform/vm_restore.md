## 虚机恢复

### 添加虚机恢复规则 {#-0}

在控制机管理界面，通过 虚拟化支持-&gt;虚机恢复，来添加/查看/删除虚机恢复规则，恢复规则添加/查看页面如下：

### 基本设置{#-1}

![说明: 1](/assets/V6.120181225180110.png)

* “名称”：客户命名的名称，便于管理；
* “源虚机”：被恢复用的源虚机名称；
* “灾备机”：存储备份数据的灾备机；
* “数据存放目录”：选择备份数据存储的路径；
* “选择备份点”：备份数据的备份时间及大小，注意这里必须选择一个备点，才能显示备份点信息，才能建立恢复规则；

### 高级设置{#-2}

![说明: 1](/assets/V6.120181225180204.png)

* “创建新虚机”：不勾选表示恢复到原来的虚机，勾选表示恢复到新创建的虚机；
* “恢复完成自动开机”: 不勾选表示恢复完成后恢复的虚机处于关机状态，勾选表示恢复完成后恢复的的虚机处于开机状态；
* “支持LAN Free”: 在LAN-FREE模式可用时，使用san方式传输；
* “虚拟机”：恢复的虚机所用的名称，不能和现有的虚机重名，不能包含特殊字符；
* “目标平台”：恢复的目标虚拟平台；
* “数据中心”：目标虚拟平台的数据中心；
* “主机名称”：目标虚拟平台的主机名称；
* “数据存储”：目标虚拟平台的数据存储磁盘；
* “处理器数量”：根据需求设定目标虚机的处理器数量；
* “处理器核心数量”：根据需求设定目标虚机的处理器核心数量；
* “内存”：根据需求设定目标虚机的内存大小；
* “MAC地址”：如果不修改这个默认值，则恢复的虚机的MAC地址会和源虚机一样，如果不希望和源虚机用一样的MAC地址，则需要在页面上删除MAC地址，虚机在创建时会分配新的MAC地址，删除MAC地址后，页面显示如下：

![说明: 1](/assets/V6.11811081039.png)

* “工作目录”：只有勾选了“创建新虚机”才会出现此选项，只有目标虚拟平台是esxi平台有此选项，表示新创建的虚机所在的目录；
* “磁盘列表”：在基本设置中选择完备份时间点后，虚拟机磁盘列表显示相对应的虚拟机磁盘，只有勾选了“创建新虚机”，才会出现“数据存储”，“磁盘路径”，“是否与工作目录一致”，此时可选择创建新虚机的磁盘存储和磁盘路径；

### 带宽控制{#-2}

![说明: 1](/assets/V6.120181225180653.png)

![说明: 1](/assets/V6.120181225172053.png)

当在某些情况下，用户想限定备机使用的带宽，可以通过带宽控制来实现。
选定某个想要限制带宽的时间段，点击单选框“限制带宽”，跳出窗口可以选择限制的带宽范围，其中0代表停止传输，就是说在这个时间段内不传输数据，备份进度会维持在当前进度。
流量图中实时流量图计算得出的带宽，由于计算方法的原因，和这里的带宽会有误差。

### 组恢复{#-3}

勾选组恢复时，页面如下：

![说明: 1](/assets/V6.120181225180531.png)

* “名称”：客户命名的名称，便于管理；
* “灾备机”：存储备份数据的灾备机；
* “数据存放目录”：选择备份数据存储的路径；
* “组别名称”：备份规则的名称；
* “虚机名称”：组内需要恢复的虚机名称；

![说明: 1](/assets/V6.120181225180928.png)

* “创建新虚机”：不勾选表示恢复到原来的虚机，勾选表示恢复到新创建的虚机；
* “恢复完成自动开机”: 不勾选表示恢复完成后恢复的虚机处于关机状态，勾选表示恢复完成后恢复的的虚机处于开机状态；
* “支持LAN Free”: 在LAN-FREE模式可用时，使用san方式传输；
* “虚拟机”：如果勾选了“创建新虚机”，这个名称可以修改，不能包含特殊字符，这个名称会和备份规则名称，虚机名称组合在一起构成恢复的虚机所用的虚机名称；
* “目标平台”：恢复的目标虚拟平台；
* “数据中心”：目标虚拟平台的数据中心；
* “主机名称”：目标虚拟平台的主机名称；
* “数据存储”：目标虚拟平台的数据存储磁盘；

### 恢复规则列表 {#-4}

恢复规则列表页面如下：

![说明: 1](/assets/V6.11811081128.png)

恢复规则包含如下状态：

* “准备中”：准备恢复；
* “创建虚机中”：正在创建虚机；
* “恢复中”：显示恢复进度百分比；
* “停止”：规则停止；
* “未知”：npsvr或备机宕机出现未知状态；
* “已完成”：恢复已完成；

针对恢复规则可用的操作，从左到右如下：

* “规则列表”：查看组内虚机列表和流量图。流量图默认展示第一条虚机的流量，当选择组内其他虚机时切换显示流量图，这里注意，选择虚机前面的复选框和流量图的显示没有关系，直接选择某一行即可切换流量图，页面如下：

![说明: 1](/assets/V6.11811081129.png)

点击“规则列表”后，操作栏按钮包含：  
启动任务：启动此虚机的规则；  
停止任务：停止此虚机的规则；
查看配置：查看此虚机的配置；

![说明: 1](/assets/V6.120181225183024.png)

删除任务：删除此虚机的规则；  
查看日志：查看此虚机的日志；

![说明: 1](/assets/V6.11811081131.png)

* “查看配置”：查看恢复规则的配置；

![说明: 1](/assets/V6.120181225183024.png)

* “启动任务”：启动恢复规则；
* “停止任务”：停止恢复规则；
* “删除任务”：删除恢复规则；

注：

（1）选择完备份点才能显示备份点信息；


**注意**

* 可根据客户需求可自行定义全局的task数量，在备机软件的安装目录etc目录下新建system.conf文件，编辑system.conf文件，添加bk\_tsk\_thd=n，n为总的最大任务并发数，默认为8，最多同时只能有8条任务在执行，包含虚机备份任务，恢复任务，迁移任务(不包含瞬时恢复任务)；
* 备机软件的安装目录etc目录下system.conf文件中的i2vp_transbuffer参数，为备机与esxi之间每次传输的数据块大小，默认是4M；
* ESXI的传输量总和不能超过32M，system.conf 中 bk\_tsk\_thd \* i2vp\_transbuffer 的总数不能超过32. 
* 添加无代理备份的任务数大于全局的task数量的最大值时，debugctl.exe back task查看任务状态为pending状态，如下图：

![说明: 3](/assets/V6.036973.png)

* 控制机管理界面pending状态任务显示如下：

![说明: 2](/assets/V6.036999.png)

* npsvr.ini配置文件中的Max\_ThreadNum\_PerHost参数，控制每个esxi主机的最大并发执行规则的数目，默认值为4，此参数受限于bk\_tsk\_thd参数的值；
* 不支持包含独立磁盘的虚机的备份；
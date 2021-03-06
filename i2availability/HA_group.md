## 高可用组

6.1之后版本增加新功能——HA分组切换，组与组之间没有太多关系，同组中可以分为不同阶段切换，不同HA规则也可以处于

同一阶段，达到同时切换的目录，HA分组可支持增加，删除，修改，强制切换操作

HA分组切换界面如下：

![](/assets/V6.118042621.png)

可以将同一条HA规则分在不同的规则中，并可以创建多个组，组切换选项参数如下：

* “修改配置“：可通过此按钮修改HA分组相关配置

* “强制切换“：对HA组中包含的HA所有规则强制切换

* “删除 ”：删除此HA分组

新建HA分组界面如下：

![](/assets/V6.118042622.png)

高可用组名称 ”：HA分组的名称，方便管理

* “切换结果确认”：切换结果确认可选择是或者否；

* “是”：表示状态查询后才表示切换成功

* “否“：表示命令下发成功后就表示切换成功

* “错误处理“：错误处理可选择忽略和停止，错误一般指下发命令失败，多因连接不上节点导致的

* “忽略“：表示遇到错误时直接返回，继续执行

* “停止“：表示当前任务如果出现错误，停止当前切换任务，后续不再执行

* “高可用规则“：显示当前所有的HA规则，可选择HA规则添加到阶段中，可增加阶段或者减少阶段

* “阶段”：处于同一阶段的HA规则可同时切换，处于不同阶段的HA规则，顺序执行

**注意事项：**
```
1、此处的切换只牵扯到界面的强制切换，不能实现自动切换
2、切换的过程中不允许中途切换到其他界面，或者刷新界面，否则切换不能正常完成
```
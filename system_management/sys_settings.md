## 系统参数

### 全局参数设置 {#-0}

![](/assets/v6.1.20180413100112.png)

* “控制机地址”：这个地址不一定是控制机本身的地址，节点通过“控制机地址”来访问控制机。

* “页面刷新时间”：有些页面需要实时监控状态，“页面刷新时间”配置多久更新一次状态。在网络状况不佳的情况下，这里可以选择大一点的间隔时间，如果网络状况很好，可以用默认的间隔时间。

* “每页显示记录数”：每页显示的记录条数。

* “控制机超时时间”：设置控制机超时时间（未进行任何操作）。

* “日志保存时间”：节点/复制规则的保存时间，旧的日志将被删除，防止控制机数据库记录过多而影响访问速度。

* “邮件语言”：控制机发送邮件通知时，采用的语言。

**注意事项：**

    “页面刷新时间”和“每页显示记录数”这两个参数配置后，必须重新登录才会生效。

### 安全设置 {#-1}

![](/assets/v6.1.20180413100225.png)

* “允许尝试登陆次数”：登陆时如果用户名和密码输错的次数大于设置的参数，页面就会锁定，提示“失败锁定时间中配置的时长”之后再次登陆。

* “失败锁定时间”：用户尝试登录超过“允许尝试登陆次数”，页面锁定的时长。

* “是否开启验证码”：页面登陆时如果此选择“是”会有输入验证码的这一项。

* “限制密码复杂度”：此选项如果选择“是”创建用户或修改密码时会做用户密码复杂度检测，密码太简单不给注册。

* “密码有效期（天）”：设置密码多少天需要重置，过期后，登陆时需要重新设置密码。

* “访问时间段”：限制访问控制机的时间段。

* “会话并发数”：同时在线的用户（普通管理员，普通用户，查看用户等）数量。

* “白名单IP”：白名单，一行一个，可输入完整的地址，支持通配符，例如: 192.168.\*.\*，留空或者0.0.0.0为对所有IP开放。

### 监控参数 {#-2}

* “巡检通知”：勾选后，会根据巡检策略定时给邮箱用户以及手机用户发送巡检提醒信息。

* “巡检提醒通知策略”：按月，表示每月的第几天发送巡检信息；按季度，表示每季度的第几天发送巡检信息；
当勾选巡检通知，并配置巡检策略后，保存配置，会以当时提交的时间为初始时间来计算发送巡检通知的时间；最短通知间隔为一天（86400秒）。

* “整体状态”：勾选后，会根据策略给邮箱用户以及手机用户发送监控对象的整体状态数量，包括节点、复制规则以及高可用规则各自正常以及异常的数量。

* “整体状态通知策略”：按小时，表示间隔几小时发送一次；按天，表示间隔几天发送一次。

当勾选整体状态，并配置通知策略后，保存配置，即时就会检测监控对象的状态并进行统计，发送整体状态通知的邮件及短信，然后以这个时间为初始时间，再根据策略设置发送整体通知。



### 邮件配置 {#-3}

![](/assets/v6.1.20180413100307.png)

* “Email通知”：启用邮件通知服务。

* “SMTP的服务器地址”：SMTP的服务器地址。

* “使用SSL连接服务器”：是否使用SSL连接服务器；需要注意和SMTP服务器端口的配合。

* “开启SMTP认证”：默认需要开启，针对某些自建邮件服务器，无需SMTP认证的取消勾选。

* “SMTP的服务器端口”：通常非SSL连接和SSL连接的端口是不同的。

* “邮箱帐号”：发送邮件的帐号。

* “邮箱密码”：当用该帐号发送邮件时，SMTP服务器需要做认证。该密码用于SMTP服务器认证。

* “监控接收Email”：测试邮件接收的邮箱以及整体状态和巡检通知接收Email。

* “发送测试Email”: 利用该页面的SMTP设置，发送测试Email到当前登录用户的邮箱。当前登录用户的邮箱设置通过用户管理修改。


### 短信配置 {#-4}

![](/assets/v6.1.20180413100327.png)

* “启用短信告警”：启用短信告警功能。

* “短信平台”：目前支持阿里大于、阿里云短信平台、ESK平台（企信王）、华为消息通知服务。

* “APPKey”：需要在阿里大于/阿里云短信平台注册账号，在管理控制台中的应用管理中获取APPKey。

* “SecretKey”：阿里大于/阿里云平台中，在管理控制台中的应用管理中获取SecretKey。

* “签名名称”： 在阿里大于/阿里云的配置管理中短信通知的配置短信签名中获取签名名称。

* “ESK服务地址”： 格式： "SERVER_IP:SERVER_PORT"（例如：192.168.1.100:8080）。

* “用户名”： ESK平台用户名或华为云用户名。

* “密码”： ESK平台登录密码或华为云用户登录密码。

* “华为账户名”： 华为账户名（DomainName）不是用户名，获取方法：基本信息界面->管理我的凭证->查看“账号名”。

* “所属区域”： RegionName为cn-north-1、cn-south-1 或者cn-east-2；获取地址：https://developer.huaweicloud.com/endpoint。

* “主题的URN”： 主题的URN， 华为云控制台创建，urn串。

* “短信模板ID/NAME”：在阿里大于/阿里云的短信模板ID，华为SMN消息主题模板。

* “监控的手机”： 测试短信、整体状态以及巡检通知接收手机。

* “短信测试”：点击可测试配置正确。

**备注：**

华为消息通知服务，不是简单的SMS服务。需要先创建一个主题，所有的应用都可以发消息给这个主题，主题会通知到“订阅者”；所以和企业版现有的控制台的SMS以及通知有点不一样，需要在华为的控制台里创建主题并添加订阅。

如下是华为消息通知服务设置的主要步骤：
* 先创建一个主题：
![](/assets/CatchB8B5\(05-28-18-30-30\).jpg)

![](/assets/Catch0294\(05-28-18-30-30\).jpg)
* 再创建一个模板，类型选择短信；华为要求同时创建一个协议为Default的同名的模板：
![](/assets/Catch8F04\(05-28-18-30-30\).jpg)

* 再添加订阅，这里协议可以选择短信和邮件以及其他的：
![](/assets/Catch0294\(05-28-18-30-30\).jpg)

如下是具体的appkey、SecretKey获取:

![](/assets/V6.118042602.png)

如下是签名名称、短信模板ID:

![](/assets/V6.118042603.png)


### 短信猫 {#-5}

![](/assets/v6.1.20180413100340.png)

* “本地短信猫告警”：针对无法访问外网的用户，可以使用短信猫来接收短信告警通知。
注：需要在控制机上通过串口连接短信猫设备。

* “短信猫型号”：目前仅支持JYC311-232。

* “串口”：短信猫连接后，占用的串口号。
Windows下用COMn，例如：COM1 (Linux下也可以用，COM1表示/dev/ttyS0)。

* “波特率”：默认9600，不用修改，短信测试异常可以调整该值。Windows可以在串口属性中设置和查看。

* “监控的手机”： 测试短信、整体状态以及巡检通知接收手机。

* “短信测试”：点击可测试是否配置成功。

测试短信猫是否正常工作：

打开“串口调试助手”，在“发送的数据/字符”右边的空白框中填入：目标手机号码:编码方式:数据；例如： 18521306155:0:hello；点击手动发送，观看上方接收区域,是否有“SMS_SEND_SUCESS”打印。

[下载链接](/i2/help/串口调试助手V2.2.zip)

### 特殊参数 {#-6}

![](/assets/v6.1.20180413100352.png)

* “忽略镜像设置”：开启时会在创建复制规则时镜像设置中有跳过镜像设置。

* “在线升级”： 允许节点在线升级。

* “高可用分组切换”： 启用高可用分组切换功能；开启后，高可用菜单项会增加“高可用组”菜单。

勾选忽略镜像设置，复制规则镜像设置显示如下：

![](/assets/V6.118042604.png)





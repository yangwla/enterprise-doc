**1.2011 节点注册失败**
![](/assets/v6.040001.png)
解决办法：删除注册文件。
注册文件路径：
Linux->/etc/sdata/下
Windows x64->C:\Program Files (x86)\info2soft-i2node\etc\
Windows x86-> C:\Program Files\info2soft-i2node\etc\

**2.1020调用工作机复制进程失败**
![](/assets/v6.040002.png)
解决办法：查看工作机sfs模块、sdata进程是否正常
Linux：lsmod | grep sfs
ps –ef | grep sdata
Windows: Win + R运行msinfo32->查看软件环境->系统驱动程序->查找是否加载成功sfs模块
查看灾备管理中的复制服务是否启动 或者 Win + R 运行services.msc 查看I2-Sdata的服务

**3．2083 恢复任务添加失败**
![](/assets/v6.040003.png)
原因：版本不支持


**4.Move规则添加失败**
![](/assets/v6.040004.png)
原因：点击过快，已经成功创建了规则。

** 5.vixError=* **

24000



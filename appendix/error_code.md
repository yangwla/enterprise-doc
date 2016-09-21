## 英方软件错误代码说明

英方软件定义了如下信息/错误代码，这些代码有可能在工作机/灾备机的运行日志中看到。

| Error Code | 说明 | 错误等级 | 可能引起的原因和解决方案 |
| --- | --- | --- | --- |
| 3519 | 复制规则重新启动 | Info | 重启系统，或者用户重启规则 |
| 3520 | 复制规则重新启动完成 | Info | 镜像完成 |
| 3522 | 网络连接错误 | Info | 工作机或者灾备机网络不通或者由于其它错误导致一端断开了网络，具体要看两端前后的日志 |
| 3523 | 镜像任务被取消 | Info | 工作机端可能达到了内存和缓存磁盘的使用上限，从而主动取消镜像任务。 |
| 3524 | 连接状态改变 | Error | 这个错误通常是由其他错误引起的，需要进一步检查工作机或者灾备机报告的其他错误。 |
| 3525 | 非法的任务 | Error | 通常是由于网络原因、灾备机重启或者其它错误导致灾备端的规则状态信息缺失 |
| 3526 | 没有配置文件 | Error | 配置文件被非法删除 |
| 3527 | 获取Linux卷组失败 | Error | 指定的卷组被删除或者访问失败 |
| 3528 | 获取逻辑卷组失败 | Error | 指定的卷组被删除或者访问失败 |
| 3529 | 没有找到对应的规则信息 | Error | 通常是由于网络原因、灾备机重启或者其它错误导致灾备端的规则状态信息缺失 |
| 3530 | 文件Checksum错误 | Error | 文件不同步，尝试重新镜像 |
| 3531 | CDP 描述文件错误 | Error | CDP的desc文件格式非法；CDP的版本和软件版本不一致； |
| 3533 | 读取CDP描述文件错误 | Error | CDP描述文件未生成或者被非法删除 |
| 3534 | 写入CDP描述文件错误 | Error | CDP描述文件未生成或者被非法删除 |
| 3535 | CDP处于错误或者不完整状态 | Error | 清空cdp，重新生成CDP |
| 3536 | 读取CDP错误 | Error | CDP的版本和软件版本不一致； |
| 3540 | 读取CDP索引文件失败 | Error | CDP索引文件未生成或者被非法删除 |
| 3541 | cdp恢复时写文件失败 | Error | 磁盘满或者文件系统访问异常 |
| 3543 | 存在的CDP版本和软件不兼容 | Error | 软件版本升级，升级后的软件不兼容老的CDP； |
| 3545 | 写消息分片内容不正确 | Error |  |
| 3546 | 工作机和灾备机软件版本不兼容 | Error | 工作机/灾备机/控制机软件版本必须一致 |
| 3547 | 时间戳错误 | Error | 可能工作机修改了系统时间。 |
| 3548 | 写入CDP索引文件失败 | Error | 检查磁盘 |
| 3549 | 写入CDP数据文件失败 | Error | 检查磁盘 |
| 3550 | CDP索引文件损坏或者不完整 | Error | 清空CDP，重新生成CDP |
| 3551 | 删除快照失败 | Info |  |
| 3554 | 灾备机收到的数据包序号不对 | Info | 网络异常，灾备系统可以自我恢复 |
| 3555 | 复制文件错误 | Error | 检查灾备文件系统或者磁盘是否满 |
| 3556 | 创建逻辑卷组失败 | Error |  |
| 3557 | 格式化逻辑卷组失败 | Error |  |
| 3559 | 工作机镜像过程中打开文件失败 | Error | 检查工作机/灾备机文件系统是否可以访问 |
| 3560 | 读取文件或者目录失败 | Error | 检查灾备机文件系统是否可以访问 |
| 3563 | 备机打开文件失败 | Error |  |
| 3564 | 创建线程失败 | Error | 重启程序 |
| 3565 | 错误的消息类型 | Error | 通常由于网络传输问题或者是软件版本不一致导致。检查程序组件版本。 |
| 3566 | 卷组扩展失败 | Error | 灾备机卷组扩展失败 |
| 3568 | 收到文件或者目录改名操作 | Info |  |
| 3570 | Cdp目录下的cfg文件出错 |  | 检查文件系统是否可以访问或者磁盘满； |
| 3571 | 非法路径 | Info |  |
| 3572 | 同一任务多次提交 | Error |  |
| 3573 | 创建快照失败 | Error |  |
| 3574 | 保存文件属性信息失败 | Error | 检查文件系统是否可以访问或者磁盘满 |
| 3575 | 任务重复 | Info | 复制过程中出现重复消息，可能由断网重连引起 |
| 3576 | 灾备机路径mount重复 | Error | 灾备机在采用卷组存放数据时，一个路径被mount多次。 |
| 3578 | 写入Mirror文件列表失败 | Error | 磁盘满或者写入磁盘错误 |
| 3579 | 读取Mirror文件列表失败 | Error | 列表文件被非法删除 |
| 3580 | CDP数据库损坏或者不完整 | Error | CDP文件被非法删除或者磁盘满 |
| 3581 | 压缩错误 | Error |  |
| 3582 | 解压错误 | Error |  |
| 3583 | 挂载快照失败 | Error |  |
| 3585 | 更新namelog文件失败 | Error | 检查文件系统是否可以访问或者磁盘满 |
| 3586 | 加密错误 | Error |  |
| 3587 | 解密错误 | Error |  |
| 3588 | 任务被锁定 | Info | HA切换到灾备机之后，锁定灾备目录，不再接受来在工作机的数据。 |
| 3589 | 写镜像文件列表失败 | Error | 检查文件系统是否可以访问或者磁盘满 |
| 3590 | 读取镜像文件列表失败 | Error | 镜像文件列表文件被非法删除 |
| 3591 | 读取文件属性失败 | Error |  |
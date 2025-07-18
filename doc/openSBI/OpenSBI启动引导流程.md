整个镜像的入口是_fw_start()，进行了如下操作:
- 根据需要对镜像进行重定位。
- 清空bss段。
- 填充struct sbi_scratch结构体。
- 设置Trap Handler。
- 调用sbi_init()。

![启动引导流程](img/opensbi初始化流程.png)
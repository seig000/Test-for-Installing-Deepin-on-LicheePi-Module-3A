### H1 RISC-V实体设备LicheePi Module 3A安装deepin操作系统 测试记录
## H2 一、镜像烧录
**工具准备**

操作环境：win11  设备：LicheePi 3A  [板卡介绍](https://wiki.sipeed.com/hardware/zh/lichee/K1/lpi3a/1_intro.html)

**烧录参考**：

[Sipeed wiki](https://wiki.sipeed.com/hardware/zh/lichee/K1/lpi3a/3_burn_image.html)      [进迭时空](https://developer.spacemit.com/documentation?token=O6wlwlXcoiBZUikVNh2cczhin5d)


工具：[Titan Flasher](https://cloud.spacemit.com/prod-api/release/download/tools?token=titantools_for_windows_X86_X64)

**镜像获取**：

[deepin20240815](https://ci.deepin.com/repo/deepin/deepin-ports/cdimage/20240815/riscv64/）

下载：deepin-23-beige-preview-riscv64-musebox-20240815-115503.
  及  uboot-k1-spacemit.zip
**辅助工具：（用途后文解释）**

[Bianbu镜像包](https://archive.spacemit.com/image/k1/version/bianbu/v2.0rc2/)


**烧录过程** 
按住boot将开发板usb连接电脑，使用titan扫描设备能扫描到即可
![扫描](pictures/1.png)
本地文件需要打包好的zip格式，使用zip的话还需要再titan工具内解压，需要一定时间。
*建议手动解压完成后使用本地目录刷机
目前,如果只使用deepin的两个文件解压（*window下需使用7-zip解压）拼起来作为刷机目录的话会发现缺失配置文件:
![缺失配置文件](pictures/2.png)
解决办法是找到Bianbu能直接用titan刷机的镜像的zip，使用已经写好的配置文件解压后作为刷机目录，然后配置分区文件：
![分区配置](pictures/3.png)
将里面的文件替换为deepin两个文件解压后里面的内容，包括root\boot\u-tool等，示例如图：

![文件替换](pictures/4.png)

![文件替换2](pictures/5.png)

替换完成点击开始刷机即可，等待烧录完成

![烧录完成](pictures/6.png)

烧录成功，但是尝试开机进系统失败，接下来连接串口进行检查。


## H2 二、分区问题处理
*使用RV DebuggerPlus连接开发板
参考[sipeed文档](https://wiki.sipeed.com/hardware/zh/lichee/K1/lpi3a/4_peripheral.html)进行连接：


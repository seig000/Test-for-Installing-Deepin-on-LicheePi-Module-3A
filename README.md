# Test-for-Installing-Deepin-on-LicheePi-Module-3A
RISC-V实体设备LicheePi Module 3A安装deepin操作系统 测试记录
# 一、镜像烧录
工具准备：
操作环境：win11  设备：LicheePi 3A
[板卡介绍]+(https://wiki.sipeed.com/hardware/zh/lichee/K1/lpi3a/1_intro.html)
烧录参考：
[Sipeed wiki]+(https://wiki.sipeed.com/hardware/zh/lichee/K1/lpi3a/3_burn_image.html)
[进迭时空]+(https://developer.spacemit.com/documentation?token=O6wlwlXcoiBZUikVNh2cczhin5d)
工具：[Titan Flasher]+(https://cloud.spacemit.com/prod-api/release/download/tools?token=titantools_for_windows_X86_X64)

镜像获取：
[deepin20240815]+(https://ci.deepin.com/repo/deepin/deepin-ports/cdimage/20240815/riscv64/）
下载：deepin-23-beige-preview-riscv64-musebox-20240815-115503.
  及  uboot-k1-spacemit.zip
辅助工具：（用途后文解释）
[Bianbu镜像包]+(https://archive.spacemit.com/image/k1/version/bianbu/v2.0rc2/)

烧录过程
按住boot将开发板usb连接电脑，使用titan扫描设备能扫描到即可

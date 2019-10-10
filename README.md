# **注意**

本仓库不支持最新的macOs Catalina，我已经尝试过，得到了血的教训，千万不要作死升级！

# 写在前面

![](https://i.loli.net/2019/10/08/3s2KUNy97glHBij.png)

![](https://i.loli.net/2019/10/08/3Zv2hwMcEPqXj8z.png)

![](https://i.loli.net/2019/10/08/93aixNSAYgZI8Uz.png)

> WIFI是Intel的，全球无解，淘宝25块买的BCM43224（不带蓝牙）

# 电脑配置

- Intel I7 4900MQ - Intel HD Graphics 4600
- 16 GB RAM
- AMD FirePro M5100（免驱）
- SSD 512G
- WIFI BCM43224

# 详细安装步骤

1. 重置BIOS设置，并更新到A25（这步大部分电脑可以省略）

2. 按照下述修改BIOS设置（开机按住F12）

```
* Advanced Boot Options = Enable Legacy
* Integrated NIC = Enable
* Parallel Ports = AT
* Seial Ports = Disabled ( If you are using Dock station then Enable it - Expermental )
* Sata Opeartion = AHCI 
* Drivers = Check all
* Switchable Graphics = Enable Switchable Graphics
* Secure Boot = Disabled 
* Virtualization = Disable 
```

3. 创建U盘启动工具，这里自行解决吧，我的镜像和使用的工具：

- 黑果小兵的 [macOS 镜像](https://zhih.me/hackintosh/#/OS-images)
- 镜像写入工具：[Etcher](https://www.balena.io/etcher/)
- 分区工具：[DiskGenius](https://pan.baidu.com/s/1yutMegaDKSQa41WOdLQSbQ)

4. U盘写入镜像完毕后，使用DiskGenius打开EFI分区，删除EFI文件夹，将本仓库EFI全部复制进去。
5. 重启按住F12，选择U盘启动，届时你将可以正确安装macOs Mojave。

# 注意事项

- 如果你的显卡是AMD，请将仓库中的`/EFI/CLOVER/kexts/Other/dAGPM.kext`删除

# 相关工具

- [Hackintool](https://pan.baidu.com/s/1YNo5TH3-gJqpNumLhRG_JQ)
- [Clover Configurator](https://pan.baidu.com/s/1I54YI3pocYcJmfsgc-cINw)


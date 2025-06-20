# DELL-5410
## 电脑配置

| 规格   | 详细信息                    |
|------|-------------------------|
| 电脑型号 | DELL-5410               |
| 处理器  | Intel i5-10210U         |
| 内存   | DDR4 16GB               |
| 硬盘   | 256GB SSD（Replace 西数SN730） |
| 集成显卡 | Intel(R) UHD Graphics 630 |
| 声卡   | Realtek ALC236          |
| 网卡   | AX201                   |


## 正常功能：
1：显卡 （核显正常，独显禁用）  
2：声卡(耳机、蓝牙耳机均正常使用)  
3：hdmi输出  
4：网卡（有线网卡正常，无线网卡可以驱动，建议更换BCM94360CS2。）  
5：触摸板正常。  
6：usb全部正常。  
7：电池电量显示正常。  
8：摄像头正常使用  
9：睡眠正常。  
10：变频正常。  
11：支持原生亮度快捷键。


## 镜像下载
- [MacOS Monterey 12.5](https://osx.cx/macos-monterey-12-5-21f79.html)
- 感谢 @黑果小兵 @黑苹果社区


## 说明
- `hackintool`目录下有所需要的工具以及ACPI、BIOS等。

## BIOS设置
* General -> Boot Sequence：勾选所有Boot Sequence选项
* General -> Advanced Boot Options：取消Enable Legacy Option ROMs
* System Configuration -> SATA Operation：勾选AHCI
* System Configuration -> USB Configuration：勾选全部
* System Configuration -> Audio：勾选全部
* Secure Boot -> Secure Boot Enable：勾选Disable
* Intel Software Guard Extensions -> Intel SGX Enable：勾选Disable


## BIOS设置 For 隐项
* 将EFI-shell文件夹复制到U盘，改名为EFI，然后从U盘启动
* 设置 Pre-Allocated DVMT 为 64M:
  ***setup_var 0xf5 0x02***
* 禁用 CFG lock:
  ***setup_var 0x3e 0x00***


## 更新日志
- 2025.06.20 全新EFI

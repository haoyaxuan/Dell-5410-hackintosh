# DELL-5410

[![OpenCore](https://img.shields.io/badge/OpenCore-0.9.9-lightblue.svg)](https://github.com/acidanthera/OpenCorePkg)
[![macOS](https://img.shields.io/badge/macOS-13.6.7-orange.svg)](https://www.apple.com/macos/ventura)

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


## 说明
- `hackintool`目录下有所需要的工具以及ACPI、BIOS等。
- [OCAT_Mac](https://github.com/ic005k/OCAuxiliaryTools/releases)

## BIOS设置
* General -> Boot Sequence：勾选所有Boot Sequence选项
* System Configuration -> SATA Operation：勾选AHCI
* System Configuration -> USB Configuration：勾选全部
* System Configuration -> Audio：勾选全部
* Secure Boot -> Secure Boot Enable：勾选Disable
* Intel Software Guard Extensions -> Intel SGX Enable：勾选Disable


## BIOS设置 For 隐项
* 在引导页按空格键，进入`modGRUBShell`
1. 设置 Pre-Allocated DVMT 为 64M:

   ```
   setup_var_cv SaSetup 0xF5 0x1 0x2
   ```
  
2. 设置 Total Gfx Mem DVMT 为 MAX:

   ```
   setup_var_cv SaSetup 0xF6 0x1 0x3
   ```
3. 禁用 CFG lock:

   ```
   setup_var_cv CpuSetup 0x3E 0x1 0x0
   ```


## 更新日志
- 2025.06.20 全新EFI

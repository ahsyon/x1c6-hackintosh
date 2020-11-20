# X1C6-EFI for macOS bigsur

Thinkpad X1 Carbon 2018的OC引导EFI（config.plist需要添加自己的三码才能使用)

### 现有配置
| Name                | Specifications | Funtional or not |
| ------------------- | -----------------------------------------|---------------|
| Processor           | Intel Core i5-8250U Processor            |Fully|
| Memory              | 8GB LPDDR3 2133MHz                       |Fully|
| Storage             | Samsung NVMe SSD Controller PM981 256GB  |Replaced by **WD BLACK SN750** then work|
| Graphics            | Intel UHD Graphics 620                   |Fully with WhateverGreen.kext and properties inject|
| Display             | 14.0" FHD 1920x1080 LED IPS              |Fully|
| Audio               | Realtek Audio ALC285 codec               |Fully with AppleALC.kext and layout-id 11|
| Ethernet            | Intel(R) Ethernet Connection (4) I219-V  |Fully with IntelMausi.kext|
| WLAN & Bluetooth    | Intel(R) Dual Band Wireless-AC 8265      |Replaced by **DW1560** then work|
| MicroSD Card Reader | Generic-SD/MMC CRW USB Device            |Fully with USBPorts.kext|
| Keyboard & Trackpad | LED backlight, TrackPoint and multi-touch touchpad |Almost fully with VoodooPS2Controller.kext and SSDT-Keyboard-X1C6 patch| 
| Fingerprint         | On chip fingerprint reader               |Non-funtional|


### 正常工作的组件/功能：
- CPU变频、睿频
- 亮度和音量快捷键
- 扬声器、麦克风
- 前置摄像头
- USB端口、microSD读卡器
- 触控板手势、三个实体键、小红点
- Wi-Fi和蓝牙
- 显示器HiDPI
- 电池电量及充电状态的显示，以及系统偏好设置中的节能选项
- 功能键F7-F12（使用[MSzturc](https://github.com/MSzturc)的[ThinkpadAssistant](https://github.com/MSzturc/ThinkpadAssistant)，配套的SSDT和二进制更名已经添加好）
	
	
	> 启用HiDPI：终端执行```bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"```


### 有问题的组件/功能
- 暂无

### 无法使用的组件/功能
- 指纹识别模块

### 未经测试
- WWAN（4G）模块
- 雷电3热插拔

### 提示
- config.plist需要添加自己的三码才能使用，否则可能导致引导OC失败，请自行添加。

### 感谢
- [Acidanthera](https://github.com/acidanthera) 维护的OpenCore引导，Lilu、WhateverGreen、AppleALC等核心驱动
- [MSzturc](https://github.com/MSzturc) 编写的[ThinkpadAssistant](https://github.com/MSzturc/ThinkpadAssistant)和ACPI补丁
- [zhtengw](https://github.com/zhtengw/EFI-for-X1C6-hackintosh) 提供的EFI-for-X1C6
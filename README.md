# X1C6-EFI for macOS bigsur

Thinkpad X1 Carbon 2018的OC引导EFI（config.plist需要添加自己的三码才能使用)

### 现有配置
- CPU：i5 8250U 1.8GHz
- 显卡：UHD620 1536MB
- 内存：8GB LPDDR3 2133MHz
- 硬盘：已更换为 西部数据SN750 NVMe SSD 512MB
- 无线网卡：已更换为 DW1560

### 正常工作的组件/功能：
- CPU变频、睿频
- 亮度和音量快捷键
- 扬声器、麦克风
- 前置摄像头
- USB端口、microSD读卡器
- 触控板手势（使用VoodooRMI驱动，更流畅）、三个实体键、小红点
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

### Credits
- [Acidanthera](https://github.com/acidanthera) 维护的OpenCore引导，Lilu、WhateverGreen、AppleALC等核心驱动
- [MSzturc](https://github.com/MSzturc) 编写的[ThinkpadAssistant](https://github.com/MSzturc/ThinkpadAssistant)和ACPI补丁
- [zhtengw](https://github.com/zhtengw/EFI-for-X1C6-hackintosh) 提供的EFI
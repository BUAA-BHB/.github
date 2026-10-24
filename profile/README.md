# BHB EEGSuite

北航 BHB 团队脑电采集与分析套件。围绕自研 BLE 脑电模块，提供 Windows 浏览器上位机与 Linux 终端轻量版两条使用路径，两者共享同一套采集协议、离线数据格式与 LSL 输出。

## 组成

| 仓库 | 平台 | 说明 |
| --- | --- | --- |
| `BHB-EEGSuite`（内部） | Windows 11 | 浏览器上位机源码：采集控制、阻抗检测、tDCS、离线录制、实时可视化 |
| `BHB-EEGSuite-for-Linux`（内部） | Linux | 终端轻量版：扫描连接、EEG 采集、阻抗检测、LSL 推流、CSV/EDF 导出 |
| [BHB-EEGSuite-release](https://github.com/BUAA-BHB/BHB-EEGSuite-release) | Windows 发行 | 免安装基础包、可选范式模块与远程模块索引 |

## 能力

- BLE 设备扫描与连接，按模块名自动识别 8/16 通道
- EEG 采集（默认 500 Hz），实时显示丢包率与设备电量
- 逐通道阻抗检测，按「良好 / 偏高 / 过差」分档提示
- LSL 实时输出（`BHB-EEG` / `BHB-IMP`），可与 OpenViBE、MNE、LabRecorder 等工具联动
- 离线会话录制与 CSV / EDF 导出，支持带通滤波与 µV 换算

## 获取

普通用户请到 [BHB-EEGSuite-release](https://github.com/BUAA-BHB/BHB-EEGSuite-release) 下载最新基础包，解压后双击 `BHB-EEGSuite.exe`，浏览器会自动打开上位机页面。

开发者请按各仓库 README 配置环境后从源码运行。

> 两个源码仓库目前仅对成员可见，如需源码或合作请联系维护者。

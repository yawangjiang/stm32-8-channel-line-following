# 代码

本目录包含 STM32F103C8 智能车循迹固件及完整 Keil MDK 工程。

## 工程入口

使用 Keil µVision 打开 [Project.uvprojx](Project.uvprojx)，选择 `Target 1`。工程使用 STM32F10x 标准外设库，目标芯片为 STM32F103C8（ARM Cortex-M3）。

## 源码位置

| 目录或文件 | 用途 |
| --- | --- |
| [User/main.c](User/main.c) | 初始化外设、读取偏差并运行控制循环 |
| `Hardware/` | 八路光电循迹、电机 PWM、MPU6050、OLED 和按键驱动 |
| `Library/` | STM32F10x 标准外设库 |
| `Start/` | CMSIS、系统时钟与启动文件 |
| `System/` | 延时等系统辅助模块 |
| `Project.uvoptx` | Keil 工程选项 |

## 编译和烧录

1. 安装 Keil MDK 和对应的 STM32F1 设备支持包。
2. 打开 `Project.uvprojx`，选择 `Target 1` 并执行 Build。
3. 根据实际开发板和下载器配置下载选项，完成烧录。

引脚分配以 `Hardware/` 中的驱动和 [PCB 工程](../PCB/README.md) 为准。

`Objects/`、`Listings/`、`DebugConfig/` 和个人 `Project.uvguix.*` 文件由根目录的 `.gitignore` 排除。

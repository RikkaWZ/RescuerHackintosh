# 拯救者 14 isk 黑苹果 OpenCore


## 一、电脑配置

| 规格     | 详细信息                                   |
| -------- | ------------------------------------------ |
| 电脑型号 | Lenovo Rescuer 14-isk Laptop               |
| 处理器   | Intel Core i7-6700HQ @ 2.60G (Skylake)     |
| 内存     | 8GB 三星 DDR4L 2133MHz                     |
| 硬盘     | 128G 三星 SSD + 1T HDD                     |
| 集成显卡 | HD530 (using Intel GPU only) + ~~GTX960M~~ |
| 显示器   | FHD 1920x1080 (14 英寸)                    |
| 声卡     | 瑞昱 ALC235                                |
| 无线网卡 | 英特尔 AX200（已更换）                     |
| 主板     | Lenovo SuperX 4B                           |

## 二、注意事项

### 1、CFG 解锁

- （！！重要）为实现最佳变频与睡眠效果，本机已解锁 CFG，未解锁的需勾选 `Kernel` -> `Quirks` 下的 `AppleCpuPmCfgLock` 与 `AppleXcpmCfgLock` 设置才可使用（未做兼容性测试）。

- 实际上，解锁 CFG 不算复杂，可以参考如下链接中的方法解锁：

  > [https://zhuanlan.zhihu.com/p/266400995](https://zhuanlan.zhihu.com/p/266400995)

  对于本机的 bios，官方最新版本 0kcn36ww，在 Windows 环境下用文中提供的工具修改 Setup 下的 0x84A 为 0x01 即可完成解锁。

## 三、尚存问题

1. 与 i7 机型最匹配的 smbios 是使用相同 cpu 的 MacBookPro13,3，但实测使用此 smbios 会导致 hdmi 无法输出。尝试过多种方案仍未能解决此问题，故退而求其次使用同代无 Touch ID 的 MacBookPro13,1。
2. 首次开机后存在内屏闪烁的问题（刷新率低），点一下睡眠再唤醒刷新率恢复正常。
3. 独显 NVIDIA GTX960M 无法驱动。
4. AX200 暂时无法使用隔空投送和 SideCar。

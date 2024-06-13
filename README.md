# Beelink-SER5-MAX-Hackintosh

> Beelink SER5 `PRO` / `MAX` Hackintosh

fork [黑果小兵 Beelink-SER5-Max](https://github.com/daliansky/Beelink-SER5-Hackintosh)

# sonoma相关

使用Recovery dmg在线安装，自行配置 com.apple.recovery.boot [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html#making-the-installer-in-windows)

- nootedred驱动存在问题，动态壁纸无法使用（会造成系统间断性挂起，只有鼠标能动）
- 将核显设置为了8GB，并设置静态壁纸，挂起减少90%，涉及系统设置的仍会有卡顿
- 企业微信图片偶发性渲染错误，直接绿掉或者红掉
- 前端开发使用vscode+chrome没有问题
- Ventura没有使用多长时间，但是并没有卡顿问题，建议留在Ventura不要升级
- sonoma 需要设置 SecureBootModel 为disable
- 蓝牙/wifi功能正常，但是可能会有设备连不上蓝牙（我的akko 3098n就连不上）

本来想用来做开发，发现小毛病影响挺大的，机子退了

## 电脑配置

|   规格   |                                  详细信息                                  |
| :-------: | :-------------------------------------------------------------------------: |
| 电脑型号 |                              Beelink SER5 MAX                              |
| 操作系统 | macOS `Sonoma` / `Ventura` /  `Monterey` / `Big Sur` / `Catalina` |
|  处理器  |                         AMD 锐龙 R5-5800H 8核16线程                         |
|   内存   |                             16 GB DDR4 3200MHz                             |
|   硬盘1   |                       KINGSTON OM8PDP3512B-A01 512GB                       |
|   硬盘2   |                           可接SATA 2.5寸硬盘/SSD                           |
|   核显   |              Radeon Vega Graphics<br />显存建议设置为：3GB/4GB              |
|  显示器  |                                     无                                     |
|   声卡   |                              USB Audio Device                              |
| 无线网卡 |                 m.2 NGFF插槽，默认出厂为 `Intel AX200`                  |
| 有线网卡1 |                      Intel Ethernet Controller I225-V                      |

## 更新日志

- 3-15-2024
  - 更新 `IOSkywalkFamily.kext` 到 `v1.1.0`
  - `Sonoma` 如果想更新到 `14.4` 请务必先更新 `EFI` ，然后再安装 [OCLP](https://pan.daliansky.net/APPS/OCLP/OCLP.md)，重启后，再升级到 `14.4` 否则会出现 `WIFI` 无法启用的问题
- 9-7-2023
  - 重要更新：修复APU核显驱动卡顿问题
- 9-6-2023
  - 修复声卡驱动
    - 声卡支持输入/输出
- 8-16-2023
  - 更新 `OpenCore` 到 `v0.9.4` Release
  - 修复声卡驱动
    - 支持显示器音频输出

## 截图

![Beelink-SER5-5800H_Micphone_OK](./ScreenShots/Beelink-SER5-5800H_Micphone_OK.png)

![iterm2](./ScreenShots/HDMI-Audio.png)

![iterm2](./ScreenShots/Beelink-SER5-MAX-iTerm.png)

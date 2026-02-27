# OpenWrt for XG-040G-MD

OpenWrt firmware for NOKIA BELL XG-040G-MD

编译脚本基于 [Cairongzeng: Add support Nokia Bell XG-040G-MD](https://github.com/Cairongzeng/openwrt/tree/xg040gmd) , [Actions-OpenWrt](https://github.com/xuxin1955/Actions-OpenWrt) 修改。

* 固件使用 OpenWrt main 分支构建，包含 luci，不包含中文语言包及其他不必要的包，与其他常见的官方 image 类似，尽可能保持小体积。
* 使用 tcboot.bin 作为引导程序。
* Snapshot 分支变化频繁，固件刷入后，有一定几率无法成功启动。
* **请准备好 USB-TTL，做好随时救砖的准备**。

## 目前遇到的问题

XG-040G-MD 使用的 NAND Flash 主要有两个型号
* SkyHigh S35ML02G300: 恩山无线论坛已有人做出相对可用的 patch，稳定性还不太确定
* Fudan Micro FM25G02B: 晚期生产的，用此型号的较多。网上目前没有靠谱的 patch，Immortalwrt 编译后虽然可运行，但是稳定性较差，而且会显示大量 ecc，大家还是不要尝试了，以免造成坏块。

## Immortalwrt Snapshots
![snapshot1](snapshots/snapshot_2026-02-09_20-14-16.png)
![snapshot2](snapshots/snapshot_2026-02-09_20-14-44.png)

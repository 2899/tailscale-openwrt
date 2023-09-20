# Tailscale on OpenWRT :smiley: [![Page Views Count](https://badges.toozhao.com/badges/01GZWH4F36G14VWXT8RP9KRCYV/green.svg)](https://badges.toozhao.com/stats/01GZWH4F36G14VWXT8RP9KRCYV)

|  在OpenWRT上部署Tailscale的最简单方法 |
| ------------ |
|  已测试支持的架构：x86_64 |
|  未经测试的架构：aarch64、armv8l、armv7l、riscv64、mips、mips64、mips64le、mipsle、i386、geode |

[English](https://github.com/CH3NGYZ/tailscale-openwrt/tree/main/README.md)
- **希望你能测试这个脚本，并在issues中通知我运行的结果。我将尽快更新文档中支持的架构部分。**
- 如果您想自定义脚本内容，请fork我的仓库，切换到相应的分支，修改/usr/bin/文件，将下载链接更改为您的仓库，Github Actions会自动将修改后的内容打包到tgz中，并将其上传到当前仓库。然后修改install.sh和Readme.MD文件中的用户名以指向您的仓库。
> Note: 由于 raw.githubusercontent.com 在中国大陆被污染, 如您在安装时超时, 或重启openwrt达5分钟后tailscale自动启动失败,请考虑使用[Github代理分支/中文脚本](https://github.com/CH3NGYZ/tailscale-openwrt/blob/chinese_mainland/README.md)
------------

## 0x00 安装
```
wget --tries=5 -c -t 60 -O- https://raw.githubusercontent.com/CH3NGYZ/tailscale-openwrt/main/install_zh-cn.sh | sh
```

------------

## 0x01 卸载
- ***请注意不要在ssh连接期间卸载，因为ssh连接将丢失！使用风险自负。***

```
wget --tries=5 -c -t 60 -O- https://raw.githubusercontent.com/CH3NGYZ/tailscale-openwrt/main/uninstall_zh-cn.sh | sh
```
------------
## 0x02 升级
- ***由于该脚本通过网络直接将TailScale的可执行文件的最新版本下载到内存中，因此每次启动openwrt时都会下载最新版本。***
```
reboot
```
------------
### 特别感谢:
[adyanth [openwrt-tailscale-enabler]](https://github.com/adyanth/openwrt-tailscale-enabler) 

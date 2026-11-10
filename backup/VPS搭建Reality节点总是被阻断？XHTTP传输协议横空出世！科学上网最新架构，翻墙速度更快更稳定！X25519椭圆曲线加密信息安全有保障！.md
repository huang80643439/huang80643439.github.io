一、准备工作

1、准备域名一个，提前在Cloudflare上做好解析

2、VPS一台重置好Dibian系统

3、下载 FinalShell SSH 工具（点击下方链接即可下载）
Windows 下载：
https://dl.hostbuf.com/finalshell3/finalshell_windows_x64.exe
MacOS M芯片下载：
https://dl.hostbuf.com/finalshell3/finalshell_macos_arm64.pkg
MacOS intel 芯片下载：
https://dl.hostbuf.com/finalshell3/finalshell_macos_x64.pkg

4、梦歌自用5年的VPS官网：[【点此进入】](https://666clouds.com/aff.php?aff=209)

PS：由于市面上的VPS厂商很多，大家使用的VPS不可能完全一样，在开始教程前请放行本教程需要使用到的端口，避免按照本教程执行完后面板打不开，或者节点无法连通！
二、Debian / Ubuntu 系统安装 sudo curl
```bash
apt update && apt install -y sudo curl
```
三、安装 BBR 网络拥塞控制
```bash
sh -c 'echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf' && sh -c 'echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf' && sysctl -p && lsmod | grep bbr
```
四、安装 3X - UI 面板
```bash
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh) v3.11.0
```
五、面板设置

Xray内核版本设置

需要使用IOS小火箭（Shadowrocket）选择Xray内核版本：v26.7.28

不使用IOS小火箭（Shadowrocket）无视这一步操作

六、入站｜安全
目标
`www.apple.com:443`
SNI
`www.apple.com`
最小客户端版本
1.0.0
或者
0.0.0
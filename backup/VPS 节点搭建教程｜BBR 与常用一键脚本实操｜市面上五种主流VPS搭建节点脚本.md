本期内容包含 1 项网络优化工具BBR＋5 种VPS节点搭建方案。先了解，再按自己的需要选择
参考：https://www.xbiit.net/2026/11/vps-bbr.html

一、开启 BBR 加速（可选）
BBR 是 TCP 拥塞控制算法，实际效果取决于线路与网络环境；它不是搭建节点的必需步骤。

1. 安装常用工具
通过 SSH 登录自己的 VPS，复制下面的命令到终端，按回车。
```bash
apt update -y && apt install -y curl wget sudo socat
```
2. 打开 BBR 管理脚本
等待上一条命令执行完毕，再运行下面的命令。
```bash
wget -N "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```
3. 根据状态选择 4 或 11
显示 BBR 加速未启用：输入 4，按回车启用。
显示“BBR 启动成功”：输入 11，按回车退出，无需重复开启。
这里指系统内核已支持 BBR 的情况；如果提示内核不支持，先检查系统，不要直接照选换内核。

二、singbox全家桶一键搭建
在服务器终端粘贴下面的完整命令，按回车。
```bash
bash <(wget -qO- https://raw.githubusercontent.com/fscarmen/sing-box/main/sing-box.sh)
```

三、Xray 一键脚本（233boy）
通过 SSH 登录自己的 VPS，粘贴完整命令，按回车，等待安装完成。
```bash
bash <(wget -qO- https://github.com/233boy/Xray/raw/main/install.sh)
```

四、singbox四合一脚本（老王／eooce）
1. 运行四合一脚本
通过 SSH 登录自己的 VPS，复制完整命令到终端，按回车。
```bash
bash <(curl -Ls https://raw.githubusercontent.com/eooce/sing-box/main/sing-box.sh)
```
五、3X-UI 可视化面板
1. 运行安装命令
通过 SSH 登录自己的 VPS，粘贴完整命令，按回车。
```bash
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)
```

六、S-UI 面板搭建
1. 运行安装命令
通过 SSH 登录 VPS，在终端执行：
```bash
bash <(curl -Ls https://raw.githubusercontent.com/alireza0/s-ui/master/install.sh)
```





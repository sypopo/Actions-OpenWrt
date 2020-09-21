# Actions-OpenWrt

## 本项目包含3个构建Action

### lean-openwrt
[lean源码](https://github.com/coolsnowwolf/lede) 构建的 x86_64 固件. 

workflows: [build-openwrt-Lean.yml](https://github.com/sypopo/Actions-OpenWrt/blob/master/.github/workflows/build-openwrt-Lean.yml)

config：[config-x86-Lean](https://github.com/sypopo/diy/blob/master/config-x86-Lean)

DIY 脚本：[diy-x86-Lean.sh](https://github.com/sypopo/diy/blob/master/diy-x86-Lean.sh)


##### 默认登陆:192.168.5.1, 密码:无

##### 默认插件包含:

+ SSR Plus
+ OpenClash
+ Frps
+ 微信推送
+ Aria2
+ 硬盘休眠
+ 网络共享
+ 磁盘管理
+ ZeroTier
+ UPnP
+ 带宽监控

### Lienol-openwrt
[Lienol源码](https://github.com/Lienol/openwrt)  构建的 x86_64 固件. 

workflows: [build-openwrt-Lienol](https://github.com/sypopo/Actions-OpenWrt/blob/master/.github/workflows/build-openwrt-Lienol.yml)

config：[config-x86-Lienol](https://github.com/sypopo/diy/blob/master/config-x86-Lienol)

DIY 脚本：[diy-x86-Lienol.sh](https://github.com/sypopo/diy/blob/master/diy-x86-Lienol.sh)

##### 默认登陆:192.168.2.1, 密码:无

##### 默认插件包含:

+ PassWall
+ Frp 内网穿透
+ 微信推送
+ Aria2
+ 硬盘休眠
+ 网络共享
+ 网络唤醒
+ DiskMan 磁盘管理
+ ZeroTier


如需修改默认配置比如定制插件等，请编辑 `workflow` 文件，修改`SSH_ACTIONS`环境变量的值`false`修改为`true`。在触发工作流程后，在 Actions 页面等待执行到SSH connection to Actions步骤，复制 SSH 连接命令粘贴到终端内，连接到 GitHub Ac­tions 虚拟服务器环境。执行：`cd openwrt && make menuconfig` 编译配置。


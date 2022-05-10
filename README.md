# vitural_box
关于虚拟机的一些东西
# 阿里云服务 基于centOs7.9如何安装图形化桌面
1. 首先登录自己的阿里云服务器
 -  `ssh 用户名@服务器ip`
 -  安装图形用户界面接口X Window System
  - `yum groupinstall "X Window System"`
  - `安装图形用界面gnome`
  - `yum groupinstall "GNOME Desktop`
2. 完成以上操作，我们还要借助vnc工具来远程连接桌面
    1. 安装服务端vnc vncserver
        - `yum -y install tigervnc-server`
    2. 启动
        -  `vncserver :1` 注意这里的:1 代表vnc连接远程服务器的端口号 5901 此时需要将阿里云服务器打开安全组规则加入5901端口开放
    3. 设置密码
        - `vncpasswd 你的远程桌面密码`
3. [安装客户端VNC-server](https://www.realvnc.com/en/connect/download/vnc/)
4. 一些快捷命令
    - ```快捷命令
        1. 设置默认启动是图形化界面输入以下指令
             ln -sf /lib/systemd/system/runlevel5.target /etc/systemd/system/default.target
        2. 卸载X Window System命令
             yum groupremove "X Window System"
        3. 卸载GNOME Desktop命令
             yum groupremove "GNOME Desktop"
    ```

### 微信安装 ###
**微信安装过程如下：**

1，下载最新版本tar.gz压缩包

wget https://github.com/geeeeeeeeek/electronic-wechat/releases/download/V2.0/linux-64.tar.gz

2，解压下载的压缩包。

3，把解压的文件夹放在/opt下。

    sudo mv electronic-wechat-linux-x64/ /opt/electronic-wechat-linux-x64

4，创建终端下的快速启动命令。（在终端输入electronic-wechat可以直接启动微信）


    sudo ln -s /opt/electronic-wechat-linux-x64/electronic-wechat /usr/bin/electronic-wechat

5，创建在Dash Home下的快速启动图标，就是为软件创建一个图标，文件后缀名是.desktop。


`#Dash Home`的图标一般在两个位置（就是你的linux系统桌面图标所在的位置，我的是在/usr/share/applications）

    /usr/share/applications

`~/.local/share/applications`（用户独立配置的基本都在这里）#只要在一个位置建立图标文件即可


    sudo vi /usr/share/applications/electronic-wechat.desktop

在electronic-wechat.desktop输入以下内容，保存并退出。

    
    [Desktop Entry]
    
    Encoding=UTF-8Version=1.0Type=Application
    
    Name=Electronic WeChat
    
    Icon=electronic-wechat.png
    
    Exec=/opt/electronic-wechat-linux-x64/electronic-wechat
    
    StartupNotify=false
    
    StartupWMClass=electronic-wechat
    
    OnlyShowIn=Unity;X-UnityGenerated=true

6，为了方便后续操作，可以创建一个类似于windows快捷图标的玩意，过程大概如下：



    sudo ln -S　/opt/electronic-wechat-linux-x64/ ~/Desktop/weixin.png

7，下载一个微信的图标，我的网盘上已经为各位准备好了，只需和安装包一块下载下来即可．

在上一步链接建立好了以后，在新生成的图标上右击，选择属性（properties），在图标那个位置单击一下，选择一个下载的图标，点击open，这样替换图标完成了．建立的软连接图标就变成了类似于windows微信的图标了。

#Git 安装教程及Github 配置
此安装教程参考 

* https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git(官网) 

* http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/00137396287703354d8c6c01c904c7d9ff056ae23da865a000  (廖雪峰教程) 

本人只在 Windows 上安装过，不确定其他系统具体安装情况，大家可考虑直接浏览上述链接进行安装，别忘了后面的设置用户名、邮箱部分和配置 github 的部分) 


###Linux 
首先，输入``git``，看看系统有没有安装 Git，如果没有安装，一般会告诉你如何安装 Git 

例： 
```
$ git 
The program 'git' is currently not installed. You can install it by typing:
sudo apt-get install git 
```
###Mac
在 Mac 上安装 Git 有多种方式。 最简单的方法是安装 Xcode Command Line 
Tools。Mavericks（10.9）或更高版本的系统中，在``Terminal``里尝试首次运行``git``命令即可。如果没有安装过命令行开发者工具，将会提示你安装。 
如果你想安装更新的版本,可以使用二进制安装程序.官方维护的OSX Git安装程序可以在 Git 官方网站下载，网址http://git-scm.com/download/mac 
###Windows (MinGW)

从 https://git-for-windows.github.io 下载 msysgit，然后按默认选项安装即可。 
安装完成后，在开始菜单里找到“Git”->“Git Bash”，蹦出一个类似命令行窗口的东西，就说明 Git 安装成功！

![git bash](http://wuch15.github.io/git1.jpg)

安装完成后，还需要最后一步设置，在命令行输入：
```
$ git config --global user.name "Your Name" 
$ git config --global user.email "email@example.com"
```
通过此命令指定本地仓库对应的用记名和 Email 地址。 
注意 git config 命令的--global 参数，用了这个参数，表示你这台机器上所有的 Git 仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和 Email 地址。 


##Github配置 

首先，你要有一个 github 账号 https://github.com/

接下来，打开你的 Git 创建你的 SSH Key 秘钥对: 

    ssh-keygen –t rsa –C “emailaddress” 
    
此时会在用户主目录下的.ssh 目录中看到 id_rsa(私钥) 和 id_rsa.pub(公钥) 

登陆 Github，打开 Account Setting，进入 SSH Key 界面，点 Add SSH Key，填上任意title 并在 Key 文本框里粘贴 id_rsa.pub 中的内容并点Add Key 

![github](http://wuch15.github.io/git2.jpg)

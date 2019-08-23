# 目录

[TOC]



## Plan in 2018

2018 input

- [ ] 按时吃饭，按时睡觉.  早7晚11，健康饮食
- [ ] Year-Book >=15
- [ ] 叶大帅打卡 >=50，Total 70~100

2018 output

- [ ] 社交APP，手机控制住2h以内
- [ ] 书评量>=10，书架Get?
- [ ] 争取腹肌4-6

## TV

- [ ] 搞笑一家人 韩国
- [ ] 开卷8分钟 凤凰卫视
- [ ] 铿锵三人行 部分
- [ ] 晓说 部分

- [x] 今生是第一次 韩国
- [ ] 世上最美丽的离别 韩国
- [x] 机智牢房生活 韩国
- [x] 逃避虽可耻但有用 日剧

## 文学

- [ ] 1984
- [ ] 乌合之众
- [ ] 人性的弱点
- [ ] 阿特拉斯耸耸肩

## 健身

- [ ] 肌酸
- [ ] BCAA
- [ ] 原味脱脂希腊酸奶

## 电脑pdf

- [ ] 《WireShark 数据包分析实战》
- [ ] 《TCP/IP详解 卷一》
- [ ] 经典Spring开发Web》
- [ ] 三大框架
- [ ] 深入解析Spring MVC与Web Flow》Seth Ladd著
- [ ] Spring MVC学习指南/（美）戴克著，林仪明，崔毅

## 软件相关

### PC

- [ ] Google+360极速
- [ ] Evernote
- [ ] flux
- [ ] Pot
- [ ] 网易云
- [ ] 微信+QQ
- [ ] Notepad
- [ ] clover
- [ ] 光驱软件
- [ ] Xmind

### 音影&office

- [ ] goldwave
    音频剪切软件
- [ ] ShareX 小工具
    ShareX高级截图工具中文版是一款高级图像抓取工具
- [ ] Foto-Mosaik-Edda 多张照片拼成一张
- [ ] AndreaMosaic 多张照片拼成一张
- [ ] Picasa Google 的免费图片管理工具Picasa
- [ ] axeslide 斧子演示axeslide.com是一款操作非常简单的演示文稿制作软件
- [ ] Latex 是一种基于ΤΕΧ的排版系统
- [ ] Focusky
    Focusky，是一款新型多媒体幻灯片制作软件，操作便捷性以及演示效果超越PPT，主要通过缩放、旋转、移动动作使演示变得生动有趣
- [ ] Prezi Prezi，是一种主要通过缩放动作和快捷动作使想法更加生动有趣的演示文稿软件
- [ ] sublime
- [ ] 番茄表单
    番茄表单是一款免费好用的表单设计和数据收集分析工具，网站制作
- [ ] 麦克
    麦客CRM是一款在线表单制作工具,同时也是强大的客户信息处理和关系管理系统
- [ ] SpaceSniffer
    SpaceSniffer 是 Windows 上一款以块状树平铺直观展现磁盘空间占用情况的软件，使用简单，功能直击痛点，而且软件本体甚至不足 1 MB
- [ ] total commander 功能强大的全能文件管理器，同步文件夹
- [ ] 方方格子Excel插件（www.ffcell.com/）
- [ ] iSlide（www.islide.cc） ppt插件
- [ ] FineReport (www.finereport.com)——做表专业户必备
- [ ] FastStoneCapturecn 截图
- [ ] Snipaste 截图

### Chrome插件

- [ ] json_handle
    It's a browser and editor for JSON document.You can get a beautiful view
- [ ] oneTab
    tabChrome插件,节省95％的内存和整洁的选项卡
- [ ] vimium http://pan.baidu.com/s/1jHVOO0A
- [ ] 印象笔记 http://pan.baidu.com/s/1miDehTI
- [ ] 马克飞象
- [ ] tampermonkey  俗称“油猴子”

### 软件开发

- [ ] Visual C+++小番茄
- [ ] Visual studio

### 调试

- [ ] debugdiag
- [ ] windbg
- [ ] HttpLogBrowser
 HttpLogBrowser是一个高级的，易于使用的程序，它提供了一个简单的方法来分析在IIS或Azure中托管的网站的W3C日志。
- [ ] Network Emulator Toolkit  
    一款windows下的网络模拟器，可以模拟各种丢包或延迟的网络
- [ ] ProcDump
    介绍一个好用的抓取dump的工具-ProcDump
- [ ] Process Hacker
    是一款功能丰富的系统程序。用户只要借助该程序就可以方便，快捷地查看相关进程的速度，内存，及模块等等，除此，还可以对相关的进程进行管理工作
- [ ] CurrPorts
    (网络连接检测)是一个免费又非常好的网络连接监测工具，除了常见的列出所有 TCP/IP 和 UDP 连接，列出打开端口的应用程序，并将终止程序以外，它提供的信息十分详细，从版本到调度的服务，还能实时高亮显示新出现的程序等等

## 重装系统

- [ ] vs 2015
- [ ] mysql
1. mysql -u root -p
2. use mysql;
3. select host from user where user='root';
4. update user set host = '%' where user = 'root';
5. FLUSH PRIVILEGES;
- [ ] mysql-connector-net-6.4.3.msi
- [ ] git
- [ ] vs extends
- [ ] jdk-8u73-windows-x64 &&环境变量

## vscode github ssh

1. 首先需要检查你电脑是否已经有 SSH key
    $ cd ~/.ssh
    $ ls
2. 创建一个 SSH key
    $ ssh-keygen -t rsa -C "your_email@example.com"
    代码参数含义：
    -t 指定密钥类型，默认是 rsa ，可以省略。
    -C 设置注释文字，比如邮箱。
    -f 指定密钥文件存储文件名。
    以上代码省略了 -f 参数，因此，运行上面那条命令后会让你输入一个文件名，用于保存刚才生成的 SSH key 代码
3. 复制公钥到github
4. 测试一下该SSH key
    $ ssh -T git@github.com

### Git配置多个SSH-Key

解决方法

1. 生成一个公司用的SSH-Key
    > $ ssh-keygen -t rsa -C 'xxxxx@company.com' -f ~/.ssh/gitee_id_rsa
2. 生成一个github用的SSH-Key
    > $ ssh-keygen -t rsa -C 'xxxxx@qq.com' -f ~/.ssh/github_id_rsa
3. 在 ~/.ssh 目录下新建一个config文件，添加如下内容（其中Host和HostName填写git服务器的域名，IdentityFile指定私钥的路径）  
    ``` text
    # gitee
        Host gitee.com
        HostName gitee.com
        PreferredAuthentications publickey
        IdentityFile ~/.ssh/gitee_id_rsa
    # github
        Host github.com
        HostName github.com
        PreferredAuthentications publickey
        IdentityFile ~/.ssh/github_id_rsa
    ```
4. 用ssh命令分别测试
    >ssh -T git@gitee.com
    >ssh -T git@github.com

### cordova short

1. cordova create hello com.example.hello HelloWorld
2. cd hello
3. cordova platform add ios
4. cordova platform add android
5. cordova platform ls
6. cordova platform remove android 
    > cordova plugin add cordova-plugin-alipay-v2 --variable APP_ID=UIH.uiwebview 
    > cordova plugin add cordova-plugin-wechat@2.1.0 --variable wechatappid=wx11111b316fbd1111
    > cordova plugin remove cordova-plugin-alipay-v2
    > cordova plugin list


**bbbbbbbb**
_iiiiiiii_
~~ssss~~
[www.baidu.com][baidu]
``` text
block
```
`dfasdfasdfasfasf`
* bubu
1. aaa
2. dd
- [ ] aa
- [ ] bb
> aaaa
> fsafsadfasdf

-----

[baidu]:https://www.baidu.com/


金字塔原理.pdf
https://www.zhihu.com/question/1959468
[你极力推荐的 Chrome 扩展有哪些？](https://www.zhihu.com/question/19594682)
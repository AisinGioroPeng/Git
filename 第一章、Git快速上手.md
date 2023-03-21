# 一、在windows系统使用Git:
## 1.概述  
        要让自己的电脑克隆一个自己所创建的库，方便自己电脑上的代码同步到GitHub中你所创建的库当中，为了实现，就需要安装一个软件，Git Bash。    
## 2.GitBash：
### 说明：GitBash是Windows下的命令行工具，基于msys GNU环境，有git分布式控制版本控制工具，主要用于git版本控制，上传下载项目代码
### 下载地址：GitHub官网：http://git-scm.com/download/win，首先进入GitHub官网，下载适合自己电脑的版本，下载时候有时候特别慢，建议寻找第三方下载
### 第三方下载位置(2023.03.21暂可下载_百度网盘)：链接:https://pan.baidu.com/s/1sN5a26sMOEVSGhD9G33Pwg  提取码：aunu
### 安装：安装位置不建议在C盘，不要存在中文路径，剩下的一路next，安装完成后随便找到文件夹右键会发现有个GitBash这就证明安装好了
### 使用：
#### a.获取ssh密钥：
        打开输入:ssh-keygen -t rsa -C "Git账号"，输入之后一处要求输入y，剩下一路回车（Enter）确认就好了
        ![image](https://user-images.githubusercontent.com/96098969/226531764-6cc1bdb1-73cc-400d-9692-6ad6ee703424.png)
#### b.找到密钥生成的路径：
        C:\Users\Gaopeng\.ssh\id_rsa.pub(本机实例生成的路径，一般都是在C盘的Users用户下的.ssh中),id_rsa.pub就是我们需要的密钥了
        ![image](https://user-images.githubusercontent.com/96098969/226531705-a58acf40-8523-4171-bcbc-ba6c584e0b93.png)
#### c.绑定ssh密钥：
        现在你就需要登录到你的GitHub上边添加这个密钥
        ![image](https://user-images.githubusercontent.com/96098969/226532484-c63acb10-20d1-4ffe-9327-ab75765ad46d.png)
        将整个id_rsa.pub内容复制
        ![image](https://user-images.githubusercontent.com/96098969/226532547-a7d2abe7-25cf-4875-a600-34a51277e29b.png)
        添加成功
        ![image](https://user-images.githubusercontent.com/96098969/226532957-e09a5478-f941-4a53-b164-b98a27586298.png)
#### d.检测是否绑定成功：
        之后回到你的Git bash上边了,输入：ssh -T git@github.com,然后输入上边的代码，来检查是否成功绑定。如果输入之后选择yes出来是这样说明就成功了。
        ![image](https://user-images.githubusercontent.com/96098969/226533208-e8a65ceb-196b-44b9-b2e0-8b5941a24740.png)
#### e.设置全局账号信息：
        安装好git后，在命令行或终端中使用下面的命令可以设置git自己的名字和电子邮件。这是因为Git是分布式版本控制系统，所以，每个机器都必须自报家门：                                 你的名字和Email地址，
                git config --global user.name “git账号”
                git config --global user.email “git邮箱，注册时候的邮箱”
                ![image](https://user-images.githubusercontent.com/96098969/226533518-9377fced-b72a-4714-9ac7-140bd9c5760a.png)
#### f.代码克隆：
        下面就要将你的库克隆下来到本地电脑中，方便以后进行上传代码，链接: https://github.com/，
        ![image](https://user-images.githubusercontent.com/96098969/226533764-d29de664-eb13-4a82-bb1d-a9cdac8f857d.png)
        在库创建完成之后 会有一个网址出现在网页中，这个地址就是代码地址。git clone 命令会用的到。
        ![image](https://user-images.githubusercontent.com/96098969/226533873-3e2f8464-9f18-4689-8729-262b5fcf682c.png)
        接下来就开始选择文件存储地方了,
        ![image](https://user-images.githubusercontent.com/96098969/226533944-59c30f03-2457-4d31-bb68-5c558464b88b.png)
        git clone后边的网址就是你创建库成功之后的网址,git clone 地址（这个地址就是刚刚创建的库那个页面上代码地址）,
        在执行命令过程有时候会让你输入账号密码啥的，这个不要输错了就行！
        ![image](https://user-images.githubusercontent.com/96098969/226534130-7b6c450c-00b2-470a-a7f0-38575d8c7d5c.png)
        可以看到，指定目录已经存在了我们的库文件
        ![image](https://user-images.githubusercontent.com/96098969/226534193-c546792c-ea4e-4c48-b1bb-ddb2721c5125.png)
#### g:测试提交文件
        打开这个文件夹，然后在其中创建一个任意格式，任意名称的文件
        ![image](https://user-images.githubusercontent.com/96098969/226534277-cae38654-9e12-47bb-9fb4-663313878ab8.png)
        然后在这个文件里面右键git bash进黑框框,git add我们新增的文件
        ![image](https://user-images.githubusercontent.com/96098969/226534336-9058ffb3-c4c5-4e5f-93cb-5a24dd2e1555.png)
        之后输入然后git commit -m “cc” 引号内的内容可以随意改动，这个语句的意思是 给你刚刚上传的文件一个备注，方便查找记忆而已
        ![image](https://user-images.githubusercontent.com/96098969/226534376-416707b0-0427-4571-8186-d426d41d0267.png)
        然后在输入git push origin master,这个就代表成功了
        ![image](https://user-images.githubusercontent.com/96098969/226534433-f2523d2c-1885-4a44-be86-83098620e172.png)
        现在打开你的GitHub网站，找到你创建的库。文件上传成功。
        ![image](https://user-images.githubusercontent.com/96098969/226534485-dcb7a620-50e3-4600-9b15-c3ab0934a732.png)      
### GitBash常用命令：
        git init:初始化git,只有初始化了以后才可以使用git相关命令
        git clone:获取远程项目并下载到本地，远程库的地址在GitHub中会有提供
        git status:查看本地与修改服务器的差异
        git add:将这些差异文件添加，这样就可以提交了
        git commit -m "这里是注释"：提交更改到服务器
        git checkout master:更改到master
        git pull:将服务器最新的更改获取到本地
        git merge local master:将本地的local合并到远程的master上
        git push origin master:正式提交到远程的master服务器上
        还有git tag、git diff、git show、git log、git remote等，这些参考后期详细文档

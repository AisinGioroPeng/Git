### 1、在windows系统使用Git:
       要让自己的电脑克隆一个自己所创建的库，方便自己电脑上的代码同步到GitHub中你所创建的库当中，为了实现，就需要安装一个软件，GitBash。    
### 2、GitBash
#### 说明：
     GitBash是Windows下的命令行工具，基于msys GNU环境，有git分布式控制版本控制工具，主要用于git版本控制，上传下载项目代码
#### 下载地址：    
     GitHub官网：http://git-scm.com/download/win，首先进入GitHub官网，下载适合自己电脑的版本，下载时候有时候特别慢，建议寻找第三方下载
#### 第三方下载位置(2023.03.21暂可下载_百度网盘)：
     链接:https://pan.baidu.com/s/1sN5a26sMOEVSGhD9G33Pwg  提取码：aunu
#### 安装：
     安装位置不建议在C盘，不要存在中文路径，剩下的一路next，安装完成后随便找到文件夹右键会发现有个GitBash这就证明安装好了
#### 使用：
##### a.随便找到文件夹进入GitBash中
![image](https://user-images.githubusercontent.com/96098969/226541394-0551d4eb-3f85-4fe2-bf63-b4196f755236.png)
##### a.获取ssh密钥：
        打开输入:ssh-keygen -t rsa -C "Git账号"，输入之后一处要求输入y，剩下一路回车（Enter）确认就好了
![image](https://user-images.githubusercontent.com/96098969/226540412-866f40f5-92b8-4836-a2f1-f2f57a36116e.png)
##### b.找到密钥生成的路径：
        C:\Users\Gaopeng\.ssh\id_rsa.pub(本机实例生成的路径，一般都是在C盘的Users用户下的.ssh中),id_rsa.pub就是我们需要的密钥了
![image](https://user-images.githubusercontent.com/96098969/226540603-e014955c-4fc9-4c60-a0d9-e7c96255e12a.png)
##### c.绑定ssh密钥(现在你就需要登录到你的GitHub上边添加这个密钥)：
![image](https://user-images.githubusercontent.com/96098969/226541935-7f5c2906-b08a-43d2-a96d-88b8f20d5925.png)
将C:\Users\Gaopeng\.ssh\id_rsa.pub中的全部内容复制到Key中：
![image](https://user-images.githubusercontent.com/96098969/226542637-5e7399fd-e9ce-438f-be56-4a6b5de5dfd8.png)
![image](https://user-images.githubusercontent.com/96098969/226543007-1f69c913-4e7e-4ebb-ac7b-e5596249dfa6.png)
##### d.检测是否绑定成功：
        之后回到你的Git bash上边了,输入：ssh -T git@github.com,然后输入上边的代码，来检查是否成功绑定。如果输入之后选择yes出来是这样说明就成功了。
![image](https://user-images.githubusercontent.com/96098969/226533208-e8a65ceb-196b-44b9-b2e0-8b5941a24740.png)
##### e.设置全局账号信息：
        安装好git后，在命令行或终端中使用下面的命令可以设置git自己的名字和电子邮件。这是因为Git是分布式版本控制系统，所以，每个机器都必须自报家门：你的名字和Email地址，
                git config --global user.name “git账号”
                git config --global user.email “git邮箱，注册时候的邮箱”
![image](https://user-images.githubusercontent.com/96098969/226547511-484ab4fd-1708-4a1b-815a-5e3d17900ea0.png)
##### f.代码克隆：
        下面就要将你的库克隆下来到本地电脑中，方便以后进行上传代码，链接: https://github.com/
![image](https://user-images.githubusercontent.com/96098969/226548054-7a204161-97a1-487d-8c79-895fd2fa7f7e.png)
        在库创建完成之后 会有一个网址出现在网页中，这个地址就是代码地址。git clone 命令会用的到。
![image](https://user-images.githubusercontent.com/96098969/226548658-1fb4774e-0f68-4dd0-9241-f7fa760c58fa.png)
        接下来就开始选择文件存储地方了,
![image](https://user-images.githubusercontent.com/96098969/226549350-c0e229df-e18b-4319-94b1-b1cfec5d0755.png)
### 
git clone后边的网址就是你创建库成功之后的网址,git clone 地址（这个地址就是刚刚创建的库那个页面上代码地址）,
在执行命令过程有时候会让你输入账号密码啥的，这个不要输错了就行！
### 
![image](https://user-images.githubusercontent.com/96098969/226549462-2c8f33d0-afd4-4ac7-92d5-9a88444d9559.png)
### 
可以看到，指定目录已经存在了我们的库文件
### 
![image](https://user-images.githubusercontent.com/96098969/226549575-6eaaf910-ebad-4d26-a1e8-3811c69442d1.png)
##### g:测试提交文件
        打开这个文件夹，然后在其中创建一个任意格式，任意名称的文件
![image](https://user-images.githubusercontent.com/96098969/226550667-c9090c69-d69a-4c2e-9a72-2d6356cecc88.png)
### 
        然后在这个文件里面右键git bash进黑框框,git add我们新增的文件
![image](https://user-images.githubusercontent.com/96098969/226550890-79d3d598-0fbb-4517-b3ab-5e567f8e1238.png)
### 
        之后输入然后git commit -m “cc” 引号内的内容可以随意改动，这个语句的意思是 给你刚刚上传的文件一个备注，方便查找记忆而已
![image](https://user-images.githubusercontent.com/96098969/226551205-6824ed7a-7cba-4bc4-823f-748e74194f1b.png)
### 
        然后在输入git push origin master,这个就代表成功了
![image](https://user-images.githubusercontent.com/96098969/226534433-f2523d2c-1885-4a44-be86-83098620e172.png) 
### 
        现在打开你的GitHub网站，找到你创建的库。文件上传成功。
![image](https://user-images.githubusercontent.com/96098969/226534485-dcb7a620-50e3-4600-9b15-c3ab0934a732.png)      
### 
#### GitBash常用命令：
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
# 

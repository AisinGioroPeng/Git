一、在windows系统使用Git:
        1.概述  
                要让自己的电脑克隆一个自己所创建的库，方便自己电脑上的代码同步到GitHub中你所创建的库当中，为了实现，就需要安装一个软件，Git Bash。    
        2.GitBash：
                说明：GitBash是Windows下的命令行工具，基于msys GNU环境，有git分布式控制版本控制工具，主要用于git版本控制，上传下载项目代码
                下载地址：GitHub官网：http://git-scm.com/download/win，首先进入GitHub官网，下载适合自己电脑的版本，下载时候有时候特别慢，建议寻找第三方下载
                第三方下载位置(2023.03.21暂可下载_百度网盘)：链接:https://pan.baidu.com/s/1sN5a26sMOEVSGhD9G33Pwg  提取码：aunu
                安装：安装位置不建议在C盘，不要存在中文路径，剩下的一路next，安装完成后随便找到文件夹右键会发现有个GitBash这就证明安装好了
                使用：
                        a.获取ssh密钥：
                                打开输入:ssh-keygen -t rsa -C "Git账号"，输入之后一处要求输入y，剩下一路回车（Enter）确认就好了
                                ![image](https://user-images.githubusercontent.com/96098969/226531764-6cc1bdb1-73cc-400d-9692-6ad6ee703424.png)
                        b.找到密钥生成的路径：
                                C:\Users\Gaopeng\.ssh\id_rsa.pub(本机实例生成的路径，一般都是在C盘的Users用户下的.ssh中),id_rsa.pub就是我们需要的密钥了
                                 ![image](https://user-images.githubusercontent.com/96098969/226531705-a58acf40-8523-4171-bcbc-ba6c584e0b93.png)
                        c.
                                 

                                
                                
                        
                        
                GitBash常用命令：
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
                
                        
                                
                

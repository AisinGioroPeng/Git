# Git在使用中遇到的各种个问题



### 1.本地仓库与远程仓库保持不一致时本地无法push到远程仓库

**报错信息:**

```
To github.com:raxx/xxar.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'git@github.com:raxx/xxar.git'
```

**分析原因:**

git 提交冲突,远端代码与本地代码不一致（别人在你提交之前提交了代码，导致你本地现在的代码与远端现在的代码不一致。）

**解决方法：**

```
1. 将自己新写的代码备份到其他地方。
2. 删除本地项目里自己新写的代码。
3. git pull 下拉代码，使本地代码与远端代码一致。
4. 重新上传代码 
git add .
git commit -m "fix bug"
git push
```

**避免操作:**

下班前push代码，上班后第一件事要pull代码





### 2. Permission denied (publickey) 没有权限的publickey

**报错信息：**

```bash
git@github.com: Permission denied (publickey). Could not read from remote repository
```

**分析原因：**

​	Permission denied (publickey) 没有权限的publickey ，出现这错误一般是以下两种原因

​	客户端与服务端未生成 ssh key

​	客户端与服务端的ssh key不匹配

**解决方法：**

​	找到问题的原因了，解决办法也就有了，重新生成一次ssh key ，服务端也重新配置一次即可。

```bash
#生成公钥
ssh-keygen -t rsa -C 79610046@qq.com

#将生成的公钥加入到Github的SSH-Keys中，然后重新push或者执行其它git操作即可。
```


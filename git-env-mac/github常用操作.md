# <center>git常用操作命令</center>
#### 设置签名
```shell
设置用户名: git config --global user.name XXX
设置密码: git config --global user.name XXX@gmail.com
```
#### 本地操作
```shell
创建本地库: mkdir AAA
初始化本地库: git init 
将文档添加到暂存区: git add x.md
将文档添加到本地库: git commit -m "push message" x.md
查看git库状态信息: git status
查看详细日志信息: git log 
查看git版本日志: git reflog
切换git版本: git reset --hard 索引值
```
#### 分支操作
```shell
创建分支: git branch hot_fix
查看所有分支情况: git branch -v
切换分支: git checkout hot_fix
切换分支: git checkout master
合并分支: git merge hot_fix
合并分支出现矛盾可对文档进行修改
修改后的文档添加到暂存区: git add x.md
修改后的文档添加到本地库(注意:此次不带文件名): git commit -m "merge from hot_fix"
```
#### 链接github
```shell
查看远程仓库别名: git remote -v
成仓库别名: git remote add arigin https://....git
删除远程仓库别名: git remote rm origin
修改远程仓库地址: git remote set-url origin <remote-url>
将本地库内容添推送远程库: git push origin master/hot_fix
克隆远程库: git clone https://....git
抓取远程库: git fetch [远程库地址别名]/[远程分支名]
合并远程库: git merge[远程库地址别名]/[远程分支名]
拉取远程库(抓取+合并): git pull[远程库地址别名]/[远程分支名]
```
#### ssh登录
```shell
切换到当前用户根目录: cd ~
生成秘钥: ssh-keygen -t rsa -C XXX@gmail.com
切换到生成的秘钥文件夹: cd .ssh
读取生成的秘钥: cat id_rsa.pub
将秘钥拷贝到GitHub > setting > ssh and gpg keys > SSH keys中即可
```
#### 团队合作
```shell
邀请团队成员: github项目 > settings > manage access > Invite a collaborator(输入邀请人GitHub账号)
第三方操作(github上完成)
拷贝github甲方方仓库: fork
将修改好的文件返回给甲方: pull request
确认乙方推送的文件没问题,合并仓库: confirm merge
```

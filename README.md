# 1、使用 git 把本地代码上传/更新到 github

1 在github上新建一个仓库（已有不用再建）

2 下载仓库到本地

3 将要上传/更新的代码复制到该文件夹下

4 配置github的邮箱、用户名、输入密码

5 添加所有文件

6 提交信息

7 抓取并合并远程仓库全部内容(git pull origin master)

8 上传到远程 github

```
$ git clone https://github.com/malele4th/git_learn.git

$ git config --global user.email "malele19931203@gmail.com"
$ git config --global user.name "malele4th"

$ git add . 
$ git commit -m "add a file demo.py"
$ git pull origin master
$ git push -u origin master
```

[git教程：廖雪峰老师](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

# 2、github中的README.md图片设置

* 将图片居中
* 宽、高按比例缩小

```
<div align="center">
<img src="https://github.com/malele4th/xxx/blob/master/xxx/xxx.png" width=80% height=80% />  
</div>
```

# 3、centos系统 git push 报错解决
$ git push -u origin master

error: The requested URL returned error: 403 while accessing https://github.com/malele4th/HttpRequest.git/info/refs

fatal: HTTP request failed

```
vim .git/config

# 修改
[remote "origin"]
	url = https://github.com/malele4th/HttpRequest.git

# 为：
[remote "origin"]
	url = https://malele4th@github.com/malele4th/HttpRequest.git
```
# 4、创建Git分支
```
git branch          # 查看分支
git branch dev      # 创建分支 dev是分支名
git checkout dev    # 切换的本地分支
git push origin dev # 提交该分支到远程仓库
git pull origin dev # 从远处获取dev


步骤: 查看、创建、切换、查看、添加、提交、上传
git branch
git branch dev
git checkout dev
git branch
git add .
git commit -m "test"
git push origin dev
```

# 5、clone历史指定版本
```
git log  ## 找到版本号
git checkout b74be8e78ff*****0a15d04967  ## 就回退到指定版本了
```

# 6、从指定分支更新代码到本地
```
git pull origin <远程分支名>   # 将远程指定分支拉取到本地当前分支上
git pull origin <远程分支名>:<本地分支名>  # 将远程指定分支拉取到本地指定分支上
在克隆远程项目的时候，本地分支会自动与远程仓库建立追踪关系，可以使用默认的origin来替代远程仓库名
```


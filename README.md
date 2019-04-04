## 使用 git 把本地代码上传/更新到 github

1 在github上新建一个仓库（已有不用再建）

2 下载仓库到本地

3 将要上传/更新的代码复制到该文件夹下

4 配置github的邮箱、用户名、输入密码

5 添加所有文件

6 提交信息

7 上传到远程 github

```
$ git clone https://github.com/malele4th/git_learn.git

$ git config --global user.email "malele19931203@gmail.com"
$ git config --global user.name "malele4th"

$ git add . 
$ git commit -m "add a file demo.py"
$ git push -u origin master
```

#Git是用来做合作开发以及版本管理的工具（svn具有同类效果）

这次课程我们需要:

1.GitHub账号（http://www.gihub.com/）注册github账号激活邮箱

2.本地安装git去git官网下载git安装

#目标

创建本地远端同步仓库实现 提交 拉取  操作的联系

#步骤:(在本地创建一个空文件夹克隆远端仓库)

##1.新建文件夹

1打开本地git(右击鼠标点击Git Bash Here)

2cd到这个文件夹

3之后准备克隆远端仓库(等待后续操作完成再回过头来克隆)waiting……

##2连接github

通过ssh连接

###（1）

$ssh-keygen -t rsa -C "你的邮箱地址"可以一路回车新建ssh key

###(2)

将ssh可以写入github

找到ssh C:\users\Admiistrator.ssh（电脑用户名）下面的id_rsa.pub用sublime打开复制一下打开github登录你的账户  找到settings->SSH and GPG keys ->new SSH keys(新建一个密钥)填写tit和粘贴已经复制好的ssh key ->Add SSH key
###(3)

验证是否连接成功 $ ssh -T git@github.com

如果SSH and GPG keys里面的钥匙由黑灰色变成了绿色  证明连接成功 相反的话连接失败

##3.新建远程仓库

https://github.com/new

填写

repository neame Description

选择

.Public(公共)

勾选

√Initalzie this repository with a README(会生成一个readme.md的文件)
##4.git命令行克隆这个远端仓库git clone git@github.com:seveb/gittest.git
这个网址来自:打开github登录你的账户 找到Your repositories ->你要克隆的仓库 ->clone or download

#命令

##git clone (克隆远端仓库)

语法:

git clone yourRepositoriesAddress(ssh/https)仓库地址 一般使用ssh格式的地址

例子:

git clone git@github.com:seven/test.git

## git add(将工作区的文件添加到缓存区)

语法:

git add youFileNameExp(文件名称/也可用正则匹配('.'))

例子:

git add index.html

git add .

.是正则表达式 意思是匹配所有文件

## git commit -m (将缓存区的文件提交到本地版本库)

语法:

git commit -m "描述提交的内容"

例子:

git commit -m "完成首页"

## git push (将本地版本库的文件提交到远端版本库)

语法:

git push 

例子:

git push

## git pull(拉取远端仓库的更新)

语法:

git pull

例子:

git pull 

##特别注意:git和 github的区别

Git是一个工具 它可以搭建github这样全球性的仓库 也可以搭建公司内部的仓库

Github就是用Git搭建的全球性的开源版本库

##配置你的用户名和email

git config --global user.name "Your Name"

git config --global user.email you@example.com
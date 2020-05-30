### 正确使用GitHub的方法
> 1. fork 别人的仓库到自己的Github;
> 2. clone 自己Github下的仓库；
> 3. 在本地仓库修改代码后，push到自己的Github;
> 4. 发起pull request 到别人的仓库。

### 为什么要新建两个远程仓库，跟踪主的远程仓库，并且push到自己的远程仓库前要先pull主的远程仓库？
> 1. 能及时知道主的远程仓库的变更；
> 2. 如果和别人同时修改同一个文件，会有提示信息，方便协作开发；

### 为什么要想修改开源仓库中的代码，必须先fork？
> + 因为直接clone别人的仓库后，想要提交代码时，需要知道对方github的账号和密码。

### 命令行
远程仓库
> + 添加：git remote add 自定义仓库名 远程仓库地址
> + 查看：git remote -v
> + 删除：git remote -rm 仓库名
> + 重命名：git remote rename 旧名字 新名字

上游仓库
> + 查看：git branch -vv
> + 切换或绑定：git branch --set-upstream-to=远程仓库名/分支名 本地分支名 
>> 当出现requested upstream branch 'origin/master' does not exist，使用如下命令解决：git pull origin master --allow-unrelated-histories

本地仓库
> + 状态：git status
> + 日志：git reflog

> + 从工作区添加到暂存区：git add *
> + 从暂存区添加到版本库：git commit -m "备注"
> + 版本回退：git reset --hard commit号

> + 拉取上游仓库但不合并：git fetch
> + 拉取上游仓库并合并：git pull
> + 上传到远程仓库：git push 远程仓库名 远程仓库分支:本地分支

分支管理
> + 创建分支：git branch 分支名
> + 切换分支：git checkout 分支名
> + ***上两步合并：git checkout -b 分支名***
> + 分支合并：git merge 分支名
> + 查看本地分支：git branch
> + 查看远程分支：git branch -r
> + 查看所有分支：git branch -a
> + 删除本地分支：git branch -d 分支名
> + 删除本地的远程分支：git branch -r -d 分支名
> + 删除远程分支：需要两步
>> 1. git branch -r -d 分支名
>> 2. git push origin 空格:分支名 

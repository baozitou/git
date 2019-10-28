### 命令
远程仓库
> + 添加：git remote add 自定义仓库名 远程仓库地址
> + 查看：git remote -v
> + 删除：git remote -rm 仓库名
> + 重命名：git remote rename 旧名字 新名字

上游仓库
> + 查看：git branch -vv
> + 切换或绑定：git branch --set-upstream-to=远程仓库名/分支名 本地分支名 

本地仓库
> + 状态：git status
> + 日志：git reflog

> + 从工作区添加到暂存区：git add *
> + 从暂存区添加到版本库：git commit -m "备注"
> + 版本回退：git reset --hard commit号

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

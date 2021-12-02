# 陌生单词
- branch 分支 
- remote 远程
- origin 原始的/起源


1. git remote -v 
   1. 查看远程仓库
2. git remote rename old new
   1. 远程仓库重命名
3. git remote add `name` `remote`
   1. 添加源仓库地址为远程仓库 -name远程仓库名称 remote远程仓库地址
# 基础工作流
- git clone `repository`
    - 克隆仓库 `repository`仓库地址
- git add `pathspec` 
    - 提交到暂存区 `pathspec`文件路径
    - git add . 将所有更改提交到暂存区,`.`代表所有文件
- git commit -m ""
    - 提交到本地仓库 双引号里写提交了什么
- git status
    - 查看当前文件的状态
- git push `remote` `branch`
    - 提交内容到远程仓库 `remote` `branch`
- git branch
    - 查看分支
- git branch `name` / git checkout -b `name` 
    - 创建一个分支  /   创建并切换分支
- git checkout `name`
    - 切换一个分支
- git branch -d `name` / git push -d `origin` `branch`
    - 删除本地分支 / 删除远程分支
# 本地版本库回退
- git log / git reflog
    - 查看你做了哪些提交
- git checkout -- `file`
    - 撤销`工作区`修改只能回退没有提交到暂存区的内容 `file`文件名
- git reset --hard `params`
    - git reset --hard HEAD^
        - 一个^表示回退一个版本
    - git reset --hard HEAD~2
        - 数字是几就回退几个版本
    - git reset --hard `版本号`
        - 回退到指定的版本号
# 分支合并&处理冲突
- git merge `branch`
  - 无冲突合并
- git merge `branch`
    - 解决冲突
        - git add `pathspec`
        - git commit -m ""
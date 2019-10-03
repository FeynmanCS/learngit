1. 设置Git
```
git config --global user.name [username]
git config --global user.email [user_email@xxx.com]
```

2. 常见命令
- git init
    + 初始化Git仓库
- git add [filenames]
    + 添加文件到仓库
- git commit -m "descriptive message"
    + 推送到分支
- git status
    + 查看仓库当前状态
- git diff [filename]
    + 查看文件变化
- git log
    + 查看commit日志
- git reset --hard HEAD^
    + 回退到上一个版本
- git reset --hard [commit id]
    + 跳转到指定id的版本
- git reflog
    + 查看版本跳转的历史
- git checkout -- [filename]
    + 丢弃工作区的修改(未添加到stage)，退回到stage状态
- git reset HEAD -- [filename]
    + 将Stage中最新版本的文件回退到工作区
    + 如果已经git add文件，可先退回工作区，再用checkout丢弃修改
    + 如果已经git commit, 应先退回上一个版本，再退回工作区，最后丢弃修改
git rm [filename]
    + 删除stage中的文件

3. 基本概念
- 工作区：本地的工作环境
- 版本库：分为暂存区和分支两个部分
    + add将工作区文件**复制**到暂存区
    + commit将暂存区文件一次性**移动**到分支
- 远程仓库：Github
    `cd ~`
    `ssh-keygen -t rsa -C [email]`
    将`id_rsa.pub`文件中的内容复制到Github中SSH Key的值

4. 远程库操作
```
# 0. 在Github上建立好新repo，不添加Readme

# 1. 关联远程库
git remote add origin https://github.com/[Username]/[repo-name].git
# 这里使用https协议，也可以使用ssh:git@github:[Username]/[repo-name].git

# 2. 第一次推送master分支所有内容
git push -u origin master

# 3. 推送最新修改
git push origin master

# 4. 从远程库克隆：可以克隆别人的repo
git clone git@github:[Username]/[repo-name].git
```

5. 分支管理
```
# 查看分支
git branch

# 创建分支
git branch [name]

# 切换分支
git checkout [name]
git switch [name]

# 创建+切换分支
git branch -b [name]

# 合并[name]到当前分支
git merge [name]

# 删除分支
git branch -d [name]

# 解决冲突
git status # 查看冲突文件
# 手动解决冲突，然后再`add`和`commit`

# 查看合并分支情况
git log --graph

```




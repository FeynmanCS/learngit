1. 设置Git
```
git config --global user.name [username]
git config --global user.email [user_email@xxx.com]
```

2. 常见命令
git init
    初始化Git仓库
git add [filenames]
    添加文件到仓库
git commit -m "descriptive message"
    推送到分支
git status
    查看仓库当前状态
git diff [filename]
    查看文件变化
git log
    查看commit日志
git reset --hard HEAD^
    回退到上一个版本
git reset --hard [commit id]
    跳转到指定id的版本
git reflog
    查看版本跳转的历史
git checkout -- [filename]
    丢弃工作区的修改(未添加到stage)，退回到stage状态
git reset HEAD -- [filename]
    将Stage中最新版本的文件回退到工作区
    如果已经git add文件，可先退回工作区，再用checkout丢弃修改
    如果已经git commit, 应先退回上一个版本，再退回工作区，最后丢弃修改





3. 基本概念
- 工作区：本地的工作环境
- 版本库：分为暂存区和分支两个部分
    + add将工作区文件**复制**到暂存区
    + commit将暂存区文件一次性**移动**到分支



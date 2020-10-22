# Git与GitHub的交互

## Git 常用命令速查表

![11455432-669c33b411d979df](image\11455432-669c33b411d979df.jpg)

## Git仓库的三大区域

![document-uid310176labid9805timestamp1548755776759](image\document-uid310176labid9805timestamp1548755776759.png)

## 基础操作

**克隆 GitHub 上的仓库到本地 :** 

- `git clone <url>`



**一次完整的修改、提交、推送操作 ：**

1. `git add .`
2. `git commit -m '修改注释'`	
3. `git push`

- **查看工作区被跟踪的文件的修改详情：**
  - `git diff --cached`

- **撤销暂存区的修改：**
  - **单个：**`git revert -- [文件名]`
  - **全部：**`git revert --`
- **查看提交历史：**
  - **全部：**`git log`
  - **n个：**`git log -n`

​	

**配置个人信息：**

1. `git config --global user.email "电子邮箱"`
2. `git config --global user.name "GitHub名字"`

- 查看配置信息：
  - `git config -l`
- 查看Git的配置文件
  - `cat -n ~/.gitconfig`



**版本回退：**

- **回退一次：**`git reset --soft HEAD^`
- **回退n次：**`git reset --soft HEAD~n`
- **提交时间线分叉：**
  - 本地仓库的 master 分支与远程仓库的 origin/master 分支在提交版本上会有了冲突
  - 若此时需要推送，则要强制推送：`git push -f`



**本地仓库 commit 变化记录：**

- **查看记录：**`git reflog`
- **修改本地仓库commit：**
  - `git reset --hard [版本号]`
  - `git reset -hard HEAD@{n}`


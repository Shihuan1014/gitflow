#### Git基础

一、Git仓库相关

+ 起步
  + git init初始化git仓库
  + git clone克隆现有仓库

+ 状态
  + untracked未跟踪状态
  + git add与.gitingore
  + 已修改状态 modified
  + 已暂存状态 staged，跳过暂存区可用 git commit -a
  + 已提交状态 commit，会生成快照放入git仓库
  + git status (-s)
+ 历史
  + git log (-p) (--pretty=oneline) (--graph) (--stat) (-2) (--since=1 day)
  + git diff (--staged)
+ 移除
  + git rm (--cached) file

+ 撤销
  + 撤销提交 git commit --amend，将当前提交替换上一次提交
  + 撤销文件的暂存区 git restore --staged file , 其实是从版本仓库中拿文件替换到暂存区的文件，不会修改工作目录的文件
  + 撤销文件的修改 git checkout -- file (检出仓库的文件替换工作目录的文件)

+ 远程仓库
  + git remote -v
  + git remote add xxx git@github:xxx/xxx
  + git remote show xxx
  + git clone
  + git pull (会加载本地没有的版本，并将最新版本合并本地代码)
  + git push (本地代码版本必须是最新的才能push上去)
  + git fetch (该指令并不会修改工作目录的文件，而是要开发者自行合并)
+ 标签
  + git tag (-l regex正则)
  + git tag -a xxx -m "注释"
  + git tag xxx (轻量级tag)
  + git show xxx  (显示tag信息)
  + git tag -a xxx SHA1部分 (追加历史tag)
  + git push remote_name tag_name (把标签推到远程仓库)

Shihuan1014提交
# Git Command

git init
git add *.c
git add LICENSE
git commit -m 'initial project version'
git status
git status -s

```text
 M README
MM Rakefile
A  lib/git.rb
M  lib/simplegit.rb
?? LICENSE.txt
```

新添加的未跟踪文件前面有 ?? 标记，新添加到暂存区中的文件前面有 A 标记，修改过的文件前面有 M 标记。 你可能注意到了 M 有两个可以出现的位置，出现在右边的 M 表示该文件被修改了但是还没放入暂存区，出现在靠左边的 M 表示该文件被修改了并放入了暂存区。 例如，上面的状态报告显示：

```text
 README 文件在工作区被修改了但是还没有将修改后的文件放入暂存区,
 lib/simplegit.rb 文件被修改了并将修改后的文件放入了暂存区。
  而 Rakefile 在工作区被修改并提交到暂存区后又在工作区中被修改了
  ，所以在暂存区和工作区都有该文件被修改了的记录。
  ?? LICENSE.txt
```
git diff
git diff --cached
git commit
git commit -m "update"
git rm README
git rm --cached README
git mv file_from file_to
git log --pretty=oneline
git log --pretty=format:"%h - %an, %ar : %s"
git ls-remote
git log origin/master
git commit -a -m 'update'
git commit -m 'initial commit'
git add forgotten_file
git commit --amend
git reset HEAD CONTRIBUTING.md  //取消暂存的文件
git checkout -- CONTRIBUTING.md

git push origin [tagname]
55555555555

git clone https://github.com/schacon/ticgit
git remote
git remote -v
git remote add pb https://github.com/paulboone/ticgit
git remote -v
git push origin master //git push [remote-name] [branch-name]
git remote show origin // git remote show [remote-name] 
git remote rename 
git rm rename git log --oneline --decorate
git log --oneline --decorate --graph --all
git checkout -b iss53
git branch
git branch -version

git branch testing
git checkout testing
git push origin master
git log --pretty=format:"%h - %an, %ar : %s"
git remote show origin
git branch -vv 本地分支
git branch -a  所有分支（本地+远程）
gitk --all

git log remotes/origin/master --pretty=format:"%h - %an, %ar : %s"
> 本文主要是记录一些Git的配置和命令。

### 安装Git

1. \\10.3.2.11\dti\FileServer\WangYuchao_WH\Git-2.24.1.2-64-bit.exe

### 基本使用

#### 设置用户名及邮箱

第一次打开Git时,首先要在Git上设置username和email；

```
$ git config --global user.name “yuchao.wang” #与注册的账号邮箱一致；
$ git config --global user.email "yuchao.wang@united-imaging.com"
```

#### 获取远程分支代码

```
$ git clone <git registry path>
```

#### 修改文件后再次提交

```
$ git add –A # 添加修改文件到临时空间
$ git commit -m “blog, git use” # 添加本地仓库和添加备注
$ git tag v2 # 打标签
$ git push origin master # 上传到服务器的master
$ git push origin --tags # 上传标签到服务器
```

#### 获得最新的代码：

```
$ git pull origin
```

获得指定版本的源码

```
$ git checkout <branch_name>
```

#### 查看所有分支

```
$ git branch --all # 本地主分支：master；远程主分支origin/master
```

#### 创建本地分支

```
$ git branch bak # 创建本地分支
$ git branch # 查看本分支；"*"号表示当前所在分支
```

#### 发布新分支

将本地新建的bak分支同步到远程服务器

```
$ git push origin bak # 这样远程仓库也有一个bak分支了
$ git checkout bak # 切换到bak分支操作
```

第一种情况：bak分支开发完成，合并到主分支：

```
$ git checkout master # 切换到主分支
$ git merge bak # 把bak分支的更改和master合并
$ git push # 提交主分支代码远程
$ git checkout bak # 切换到bak远程分支
$ git push # 提交bak分支到远程
```

第二种情况：bak分支没开发完，推送保存，下次再开发：

```
$ git add -A # 添加修改文件到临时空间
$ git commit -m “bak branch” # 提交本地bak分支仓库
$ git push # 提交bak分支到远程
```

#### 删除分支

```
$ git checkout master  #切换到master分支
$ git branch -D bak # 用branch -D 删除目标分支
$ git branch # #查看删除后的本地分支
```

#### 删除远程bak分支，危险命令

```
git push origin :bak
```

#### 草稿箱

```
$ git stash save "save message"  # 执行存储时，添加备注，方便查找，只有git stash 也要可以的，但查找时不方便识别。
$ git stash list  # 查看stash了哪些存储
$ git stash show # 显示做了哪些改动，默认show第一个存储,如果要显示其他存贮，后面加stash@{$num}，比如第二个 git stash show stash@{1}
$ git stash show -p # 显示第一个存储的改动，如果想显示其他存存储，命令：git stash show  stash@{$num}  -p ，比如第二个：git stash show  stash@{1}  -p
$ git stash apply # 应用某个存储,但不会把存储从存储列表中删除，默认使用第一个存储,即stash@{0}，如果要使用其他个，git stash apply stash@{$num} ， 比如第二个：git stash apply stash@{1} 
$ git stash pop # 命令恢复之前缓存的工作目录，将缓存堆栈中的对应stash删除，并将对应修改应用到当前的工作目录下,默认为第一个stash,即stash@{0}，如果要应用并删除其他stash，命令：git stash pop stash@{$num} ，比如应用并删除第二个：git stash pop stash@{1}
# git stash drop stash@{$num} # 丢弃stash@{$num}存储，从列表中删除这个存储
# git stash clear ：删除所有缓存的stash
```

**新增的文件，直接执行stash是不会被存储的**

**git add 只是把文件加到git 版本控制里，并不等于就被stash起来了，git add和git stash 没有必然的关系，但是执行git stash 能正确存储的前提是文件必须在git 版本控制中才行。**


查看git流程图 

![1.png](/.attachments/1-95b15eb6-508d-4bcb-af6f-2b82572ac1d8.png)

常用命令

```
$ git clone <git registry> # 拉取远程代码
$ git branch -b <branchName> # 创建并切换本地分支
$ git add . #提交当前路径下所有的修改文件到暂存区
$ git commit -m “bak branch” # 提交本地bak分支仓库
$ git push origin <branchName> #创建远程分支并将本地分支提交
$ git pull origin <branchName> #获取远程分支最新代码
$ git branch -v #查看当前所有本地分支
$ git branch -a #查看远程所有分支
$ git merge bak # 把bak分支的更改和当前分支合并
$ git cherry-pick <git hashcode至少六位> #合并某个提交的版本
$ git status #查看仓库状态;
$ git diff XX #查看XX文件修改了那些内容;
$ git log #查看历史记录;
$ git reflog #查看历史记录(含回退纪录)；
$ git reset –hard HEAD^ #回退到上一个版本;
$ git reset –hard HEAD~ #回退到上一个版本;
$ git reset –hard HEAD~100 #回退到100个版本;
$ git reset -hard <git hashcode至少六位> #回退到这个hash code的版本
$ git reset HARD filename # 强制将某个提交文件移除暂存区
$ git checkout – XX #把XX文件在工作区的修改全部撤销；
$ git rm XX #删除XX文件跟踪；
```








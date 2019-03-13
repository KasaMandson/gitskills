# Learn Git

## 一、基本用法

#### 1.1 初始化Git版本仓库

git init , 初始化.git仓库

git config --global user.name "xxx" , 初始化全局username

git config --global user.email "xxx@xxx.com" , 初始化全局useremail

#### 1.2 查看版本库状态和提交/操作的日志

git status , 查看git版本库的状态

git log , 查看git提交日志

git log --oneline , 只显示前几位hash的提交日志

git reflog , 查看git命令操作日志，类似终端下的history

#### 1.3 撤销修改

git reset --hard HEAD^ , 返回当前版本(HEAD)的上一个版本

git reset --hard HEAD~5 , 在当前版本往上返回五个版本

git reset --hard commit_id , 根据commit的hash值来返回对应的版本

git checkout -- file

1.当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

2.当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。

3.已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

#### 1.4 删除文件

rm file

git rm file

1.如果你用的rm删除文件，那就相当于只删除了工作区的文件，如果想要恢复，直接用git checkout -- file就可以
2.如果你用的是git rm删除文件，那就相当于不仅删除了文件，而且还添加到了暂存区，需要先git reset HEAD file，然后再git checkout -- file
3.如果你想彻底把版本库的某文件删除掉，先git rm file，再git commit -m "xxx" 就可以了



## 二、远程仓库

#### 2.1 添加远程仓库

git remote add origin git@server-name:path/repo-name.git ssh协议

git remote add origin https://server-name:path/repo-name.git http协议

之后使用
git push -u origin master 第一次推送master分支的所有内容

后续修改master分支后只需要使用 git push origin master 进行提交即可



#### 2.2 从远程库克隆

git clone https://github.com/KasaMandson/gitskills.git http协议

git clone git@github.com:KasaMandson/gitskills.git ssh协议



## 三、分支管理
Creating a new branch is quick. This is dev branch ~

I am testmerge branch, just test merge ~

WTF Y ? HOW TO and simple.


#### 3.1 创建与合并分支

Git鼓励大量使用分支：

查看分支：`git branch`

创建分支：`git branch <branch_name>`

切换分支：`git checkout <branch_name>`

创建+切换分支：`git checkout -b <branch_name>`

合并某分支到当前分支：`git merge <branch_name>`

删除分支：`git branch -d <branch_name>`











待续...

```
Thanks to [廖雪峰](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000). 
```

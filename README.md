# Learn Git

git init , 初始化.git仓库

git config --global user.name "xxx" , 初始化全局username

git config --global user.email "xxx@xxx.com" , 初始化全局useremail

git status , 查看git版本库的状态

git log , 查看git提交日志

git log --oneline , 只显示前几位hash的提交日志

git reflog , 查看git命令操作日志，类似终端下的history

git reset --hard HEAD^ , 返回当前版本(HEAD)的上一个版本

git reset --hard HEAD~5 , 在当前版本往上返回五个版本

git reset --hard commit_id , 根据commit的hash值来返回对应的版本



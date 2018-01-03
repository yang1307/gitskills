# gitskills
1.安装Git 进入Git Bash
> $ git config --global user.name "Your Name"   
> $ git config --global user.email "email@example.com"

2.创建版本库

> $ mkdir learngit  
> $ cd learngit  
> $ pwd   
/Users/michael/learngit  
*pwd用于显示当前目录，learngit为设置的版本库名字*   
> $ git init  
*把目录变成Git可管理的仓库*

3.把文件添加到版本库

> $ git add readme.txt  
> $ git commit -m "wrote a readme file"  
[master (root-commit) cb926e7] wrote a readme file  
 1 file changed, 2 insertions(+)  
 create mode 100644 readme.txt  
 *readme.txt要放在learngit目录下，add是把文件添加到仓库，commit是把文件提交到仓库， -m 代表本次提交修改的说明。支持多次add一次commit*
 
 4.时光穿梭机
 
 > $ git status   *查看仓库当前状态，会告诉你哪些文件被修改过*  
 > $ git diff  *可查看修改内容*

# gitskills
> $ git config --global user.name "Your Name"   
> $ git config --global user.email "email@example.com"   
> $ mkdir learngit  
> $ cd learngit    
> $ pwd    
*pwd用于显示当前目录，learngit为设置的版本库名字*   
> $ git init *把目录变成Git可管理的仓库*  
> $ git add readme.txt  
> $ git commit -m "wrote a readme file"   
 *readme.txt要放在learngit目录下，add是把文件添加到仓库，commit是把文件提交到仓库， -m 代表本次提交修改的说明。支持多次add一次commit*  
 > $ git status   *查看仓库当前状态，会告诉你哪些文件被修改过*  
 > $ git diff  *可查看修改内容*  
 > $ git log  *版本回退前先用该命令查看提交历史，显示最近到最远的提交日志，确定回退到哪个版本。加上 --pretty=oneline 参数可显示commit id（版本号）*
 > $ git reset --hard HEAD^  *用HEAD表示当前版本，上一个版本就是HEAD^。上上一个版本就是HEAD^^*  
 > $ git reset --hard 3628164  *也可以用id号进行版本回退*  
 > $ git cat readme.txt  *查看readme文件*  
 > $ git reflog  *可用来记录你的每一个命令，找回commit id即可继续完成版本回退*     

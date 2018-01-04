# gitskills
$ git config --global user.name "Your Name"   
$ git config --global user.email "email@example.com"   
$ mkdir learngit  
$ cd learngit    
$ pwd    
*pwd用于显示当前目录，learngit为设置的版本库名字*   
$ git init *把目录变成Git可管理的仓库*  
$ git add readme.txt  
$ git commit -m "wrote a readme file"   
 *readme.txt要放在learngit目录下，add是把文件添加到仓库，commit是把文件提交到仓库， -m 代表本次提交修改的说明。支持多次add一次commit*  
$ git status   *查看仓库当前状态，会告诉你哪些文件被修改过，可用于分支合并冲突时内容的查看*  
$ git diff  *可查看修改内容*  
$ git log  *版本回退前先用该命令查看提交历史，显示最近到最远的提交日志，确定回退到哪个版本。加上 --pretty=oneline 参数可显示commit id（版本号）*
$ git reset --hard HEAD^  *用HEAD表示当前版本，上一个版本就是HEAD^。上上一个版本就是HEAD^^*  
$ git reset --hard 3628164  *也可以用id号进行版本回退*  
$ git cat readme.txt  *查看readme文件*  
$ git reflog  *可用来记录你的每一个命令，找回commit id即可继续完成版本回退* <br>
$ git diff HEAD -- readme.txt  *可以查看工作区与版本库里面最新版本的区别* <br>
$ git checkout -- readme.txt  *把readme.txt文件在工作区的修改全部撤销，这里有两种情况：一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。总之，就是让这个文件回到最近一次git commit或git add时的状态*<br>
$ git reset HEAD readme.txt *用命令git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区  git reset命令既可以回退版本，也可以把暂存区的修改回退到工作区。当我们用HEAD时，表示最新的版本。*<br>
$ rm readme.txt *删除无用的文件*<br>  *现在你有两个选择，一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit 另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本* <br>
$ git remote add origin git@github.com:yang1307/learngit.git *关联github上的仓库* <br>
$ git push -u origin master  *把本地内容推送至远程库。由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令* <br>
$ git push origin master  *至此简化了今后的提交步骤*  <br>
$ git clone git@github.com:yang1307/gitskills.git  *先在github上建立新的远程库，克隆该远程库* <br>
$ git checkout -b dev  *创建并切换至dev指针* <br>
$ git branch  *git branch命令会列出所有分支，当前分支前面会标一个\*号* <br>
$ git checkout master  *dev分支工作完成后切换回master分支* <br>
$ git merge dev  *合并某分支到当前分支* <br>
$ git branch -d dev  *删除 dev* <br>
$ git log --graph --pretty=oneline --abbrev-commit  *查看合并图* <br>
$ git merge --no-ff -m "merge with no-ff" dev  *禁用fast forward的合并模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信息*  <br>
$ git stash  *Git还提供了一个stash功能，可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作* <br>
$ git stash list  *一是用git stash apply恢复，但是恢复后，stash内容并不删除，你需要用git stash drop来删除；另一种方式是用git stash pop，恢复的同时把stash内容也删了：* <br>
如果要丢弃一个没有被合并过的分支，可以通过git branch -D <name>强行删除 <br>
$ git remote  *查看远程库的信息，用git remote, 用git remote -v显示更详细的信息* <br>
$ git push origin master  *推送分支，就是把该分支上的所有本地提交推送到远程库。推送时，要指定本地分支，这样，Git就会把该分支推送到远程库对应的远程分支上* <br>
$ git checkout -b dev origin/dev  *要在dev分支上开发，就必须创建远程origin的dev分支到本地，于是他用这个命令创建本地dev分支* <br>

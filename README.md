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
$ git status   *查看仓库当前状态，会告诉你哪些文件被修改过*  
$ git diff  *可查看修改内容*  
$ git log  *版本回退前先用该命令查看提交历史，显示最近到最远的提交日志，确定回退到哪个版本。加上 --pretty=oneline 参数可显示commit id（版本号）*
$ git reset --hard HEAD^  *用HEAD表示当前版本，上一个版本就是HEAD^。上上一个版本就是HEAD^^*  
$ git reset --hard 3628164  *也可以用id号进行版本回退*  
$ git cat readme.txt  *查看readme文件*  
$ git reflog  *可用来记录你的每一个命令，找回commit id即可继续完成版本回退* <br>
$ git diff HEAD -- readme.txt  *可以查看工作区与版本库里面最新版本的区别* <br>
$ git checkout -- readme.txt  *把readme.txt文件在工作区的修改全部撤销，这里有两种情况：一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。总之，就是让这个文件回到最近一次git commit或git add时的状态*<br>
$ git reset HEAD readme.txt *用命令git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区  git reset命令既可以回退版本，也可以把暂存区的修改回退到工作区。当我们用HEAD时，表示最新的版本。*<br>
$ rm readme.txt *删除无用的文件*<br>  *现在你有两个选择，一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit 另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本*

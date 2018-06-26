This is my first git file.

learning note

******************
git setup
******************
1__setup git from git web:https://git-scm.com
2__config git user & email by CMD of windows:
	git config --global user.name "Your Name"
	git config --global user.email "email@example.com"

******************
create git repository
******************
1__mddir & cd to the dir
2__create git repository by CMD cmd：
	git init


******************
version management
******************
git add <filename>					____add file to buffer
git rm <filename>					____remove file to buffer
git commit -m "noticement"			____push buffer file to workspace
git push							____push workspace file to master
git log								____view git version info & commit id
git log --pretty=oneline			____oneline display of "git log"
git reflog							____display all your operation of version, expect "push".You can find forward version which has been gone back

******************
version go back
******************
git reset HEAD <filename>			____undo buffer file, it will not change actually file, just clean buffer file which is not visible
git reset --hard HEAD				____go to current version, commit & before any change
git reset --hard HEAD~				____go to last version
git reset --hard HEAD~~				____go to last 2 version
git reset --hard HEAD~10			____go to last 10 version
git reset --hard <commit id>		____go to corresponding commit id version
git checkout -- <filename>			____undo modify, all modify back to buffer or workspace


******************
remote repository
******************
1__generate SSH key by CMD:
	ssh-keygen -t rsa -C "<youremail@example.com>"
	dir .ssh will generate 2 file: id_t=rsa & id_rsa.pub, id_rsa is private key should be secret, id_rsa.pub is public key to identify your SSH info
2__add ssh key into github
	login in github,
	choose "account setting"
	"add ssh key": id_rsa.pub file
	comfirm
3__create new repository
	login in github,
	"new repository"
	add repository name
	create
4__link repository
	CMD:
	git remote add origin git@github.com:<github_name>/<repository_name>.git
5__first time to push master branch
	CMD:
	git push -u origin master
	
******************
repository clone
******************
CMD:
	git clone git@github.com:<github_name>/<repo_name>.git
	the cmd will auto create a repo dir
	

******************
branch management
******************
git checkout -b <branch_name>				____create new branch & switch to it
	= git branch <branch_name>				____create new branch
	+ git checkout <branch_name>			____switch to branch
git branch									____show branch, the curent branch is tag with *
git branch -d <branch_name>					____delete branch
git merge <branch_name>						____merge branch


do conflict test
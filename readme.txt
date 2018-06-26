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
git commit -m "noticement"			____push buffer file to workspace
git push							____push workspace file to master
git log								____view git operation log & edition info
git log --pretty=oneline			____oneline display of "git log"
git reset HEAD^						____go back to last version
git reset HEAD^^					____go back to last two version
git reset HEAD~10					____go back to last ten version
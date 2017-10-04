Adding files to be committed - git add <Insert File name here>

to commit the files - git commit -m "Insert commit message here"

to send the file to the repository on github - git push origin master

to connect to the respository - git remote add origin <Insert website path here>

to create a branch and switch to it - git checkout -b <insert branch name here>
git 
to switch back to master branch - git checkout master

to delete the branch - git branch -d <insert branch name here>

to push the brnach to remote repository - git push origin <insert branch name here>

to update local repository to the newest commit  - git pull

to merge another branch into your active branch (e.g. master branch) - git merge <insert branch name here>


in both cases git tries to auto-merge changes. Unfortunately, this is not always possible and results in conflicts. You are responsible to merge those conflicts manually by editing the files shown by git. After changing, you need to mark them as merged with - git add <insert file name here>

to preview changes before merging - git diff <Source branch here> <target branch here>



In case you did something wrong, which for sure never happens ;), you can replace local changes using the command

git checkout -- <filename here>

this replaces the changes in your working tree with the last content in HEAD. Changes already added to the index, as well as new files, will be kept.

If you instead want to drop all your local changes and commits, fetch the latest history from the server and point your local master branch at it like this

git fetch origin

git reset --hard origin/master

useful hints

built-in git GUI - gitk

use colorful git output - git config color.ui true

show log on just one line per commit - git config format.pretty oneline

use interactive adding - git add -i



http://rogerdudler.github.io/git-guide/

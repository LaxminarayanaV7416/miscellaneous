### Lets see how to work with git from command line
 --- Command to install git in Ubuntu ---
* $ sudo apt-get install git
* $ git --version ==> to check the version of github
* $ git <verb> --help
 (or)
* $ git help <verb>
* eg. git config --help (or) git help config
   
#### Lets see all the commands useful in git
for more details of GIT CLI visit [Link is here](https://git-scm.com/book/en/v2 "its pro git book")
* lets see how to add git user name and git user email in config
    * $ git config --global user.name "LaxminarayanaV7416"
      * To add the username to config
    * $ git config --global user.email "laxminarayana.vadnala@gmail.com"
      * to add user email address to config 
    * $ git config --list
      * to see all the configs you added as list
   * git log 
      * to see logging of our commits
 * lets consider two scenarios first being uploading files from local system to git and other being cloning online git and working (we mostly deal with this)
   * lets work first on the first scenario uploading the local respository to git server
      * git init
         * execute this command to initialize that this directory will be uploaded to git server, this will create .git file
      * git status
         * to see what all files are going to upload in git lets deal with colors now,red mean they are in working directory, green color mean they are in staging area
      * touch .gitignore
         * which creates a git ignore file and we can add what all folders and files to stop uploading to git
         * add samples files for eg. .vscode \n .pycache \n $.pyc
      * git add -A
         * to add all files to staging area (tip: see git status to see they will be in green)
      * git add filename
         * to add single file to staging area
      * git reset
         * to revert all files from staging are to working directory
      * git commit -m "Type your commit comment here!"
         * to commit the files to local storage (! you have to push to save the changes to server)
      * git diff
         * to see all changes made to the files or code
   * lets clone the other repos and start working on them
      * git clone url_or_fileaddress location_you_to_on_our_system
         * eg git clone git@github.com:LaxminarayanaV7416/webDevelopment.git . ==> . means to pwd directory
      * git pull origin master
         * to pull the origin master of the repository
      * git push origin master
         * to push the code to the repository (Woooo now u can see the changes in github)
      #### Now lets start working with the branches aspect as we are till now working on master
      * git branch
         * to see what all branches are there and green and astricks highlithed indicates the we are on that branch
      * git branch branchname
         * this function creates the branch of the master now we can work on this branch and we can commit to master later on
      * git checkout branchname
         * to the working from one branch to branchname we can use checkout to checkout that branch
      * git push -u branchname
         * to basically merge the local and remote repo's branch use the above command and it will push it to remote repo later we can use the 
      * git push branchname
         * to push the branchname to remote repo
      * git pull -u branchname / git pull branchname
         * same as abover explanation
      * git branch -a 
         * to see all sort of branches with proper explanation
      * git checkout master
         * to checkout the local master branch, pull the master branch and now follow next step
      * git branch --merged 
         * to see what branches are merged together, as we follow steps we didnt merge the branchname to master we cannot see the branchname branch in the output.
      * git merge branchname
         * now we have merged the branchname with master, perform above code(git branch --merged) again to see what all merged with branch.
      * git push origin master
         * pushes the code merged branch to remote repo.
      * git branch -d branchname
         * to delete the branchname branch from repo.
      * git push origin --delete branchname
         * to delete the branch on remote repo
#### Now lets discuss about some techniques how to revert to older versions of code if we do some huan errors.
   * git checkout filename
      * to revert back to older version if we accidentally saved the file
   * git commit --amend -m "change of commited comment Note the git history also changes"
      * changing the comment of the commit
   * git commit --amend 
      * to add extra files as well as we can change the comment instead of commiting it several times
   * git log --stat
      * to see advance log options
   * git cherry-pick hash_number_of_commit
      * to copy commit from one branch to other if at all we accidentally commited it in some different branch, Note to checkout the branch before you cherry-pick it
   * git reset --soft old_version_hash_number
      * to reset the commited changes to staging area, it wont change our saved code and dont remeove files from staging area.
   * git reset old_version_hash_number
      * this is a mixed reset and it removes the commit and removes files from staging area but dont change the new code.
   * git reset --hard old_version_hash_number
      * this will do hard reset of files and reverts the code as well
   * git clean -df
      * to get rid of untracked directories(d) and files(f), untracked means new files we may extracted newly and not present on repo or commit section.
   * git reflog
      * show the reference of log of commits with comments serially.
   * git checkout newhash
      * if we want to go ahead of new version if we are in older version
   * git revert hash_number_usually_seven_characters.
      * to revert the old hash number without changing history.
   * git diff hash_one hash_two
      * to compare two files 
   * git stash save "write your comment here!"
      * stashing is like saving them in memory but our repo stays unedited like it was after pull.
   * git stash list
      * to see the list of stashed we saved.
   * git stash apply stashcode_you_have_to_use
      * to apply those saved changes to our repository
   * git stash pop
      * to apply the latest saved stash to the repo
   * git stash drop stash_code
      * to delete the saved stash from stash list
   * git stash clear
      * NOTE : to delete all the saved stashes from list
      

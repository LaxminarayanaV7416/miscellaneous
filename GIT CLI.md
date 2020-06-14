### Lets see how to work with git from command line
```Python
# --- Command to install git in Ubuntu --- #
# $ sudo apt-get install git
# $ git --version ==> to check the version of github
# $ git <verb> --help
# (or)
# $ git help <verb>
# eg. git config --help (or) git help config
```
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

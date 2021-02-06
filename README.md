# git-notes
This repo contain all common git commands.

## Commands in lesson one 

1. To find the git version
   ```
   git version
   ```
1. To configure git username on computer
   ```
   git config --global user.name 'username'
   ```
1. To configure git email on computer
   ```
   git config --global user.email 'username@example.com'
   ```
1. To list the git configuration
   ```
   git config -l
   ```
1. To initiate a git repository
   ```
   git init <directory_name>
   ```
1. To add file from working directory to staging area for git to track.
   ```
   git add <filename>
   ```
1. To stop pushing a file to github
   ```
   touch .gitignore
   vim .gitignore
    *.pyc
    .DS_Store
    .project
   :wq
   ```
1. To add all files 
   ```
   git add .
   ```
1. To add all files from any sub-folder
   ```
   git add -A
   ```
1. To save changes to the local git repo
   ```
   git commit -m "message"
   ```
1. To check the status of git directory
   ```
   git status
   ```
1. To list the history of the commits
   ```
   git log
   ```
1. To make the output user friendly
   ```
   git log -all --graph --decorate --oneline
   ```
1. To create a new branch
   ```
   git branch <branch_name>
   OR
   git checkout -b <branch_name>
   ```
1. To check all the branches of the repo
   ```
   git branch -a
   ```
1. To change into a branch  
   ```
   git checkout <branch_name>
   ```
1. To push changes from local git repo main branch in remote repo
   ```
   git push origin main
   ```
1. To merge a branch into main branch
   ```
   git checkout main
   git merge <branch_name>
   git push origin main
   ```
1. To delete a branch after it is merged
   ```
   git branch -d <branch_name>
   ```
1. To merge without checking if it is merged or not
   ```
   git branch -D <branch_name>
   ```
1. To clone an existing repo from github
   ```
   git clone <https://git_url>
   ```
1. To pull the latest changes from github repo
   ```
   git pull origin main
   ```
1. To find the changes in commited file and new file
   ```
   git diff <file_name>
   ```
1. To reset the changes made to the local repo
   ```
   git checkout -- <filename>
   ```
1. To see the differences between staged changes and last commited changes
   ```
   git diff --staged
   ```
1. To highlight the differences
   ```
   git diff --color-words
   ```
1. How to remove all changes since last commit
   ```
   git reset HEAD --hard
   git clean -fd
   ```  


# How to create an issue
1. First go to the github project. 
1. Click the issue tab
1. Click new issue
1. Give an issue heading small e.g. 'Add intoduction section'
1. Save the issue.

# How to work an issue
1. First go to github project
1. Fork the project to your github account
1. Click the issues tab again
1. Click the issue you want to work on
1. Once you decide to work on it, assign it to yourself from right menu
1. Now to start working on it you need to clone that project
1. After cloning make a new branch in the following way
   ```
   # If the issue name is `Add intoduction section` having number 10
   # Then the branch name will be
   git branch 10-add-introduction-section

   # Now to commit the changes, you will do
   git commit -m 'Issue #10: introduction section added'
   
   # To push the changes to the branch
   git push origin 10-add-introduction-section

   # Now you can make a pull request to the project developer
   ```
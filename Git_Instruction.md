![logo](git_logo.jpeg)
# <span style="color:yellow"> Git Setup Instruction (Simple version)</span>

Hello!

I'm happy to meet you in the Git Setup Instruction (Windows system type).

*<span style="color:grey">So, 1st of all please make a cap of coffe or tea, that you like more, and just relax about 1min for refresh your mind and start to do below actions in your best mood.* </span>

## 1. PC System options initialization.

write text `git version` into terminal:

if git installed to your PC, you will see message with version of programm.
Else you have error message. Next please make below actions:

You need know PC system type (32 or 64-bit). Please check MyComputer options and System type.


## 2. Setup file download.

Please open the oficial [web-site](https://git-scm.com/downloads) for the last version to download same with your PS System type (32 or 64bit). Make download to your PC.


## 3. Git installation.

+ Now you will start to install the Git programm from the downloaded .exe file. *You can keep recomended options in time of each step installation. Push '`Next`' button till message with finished install of Git.*

+ Please start __Git__ for next time checking that installaion was correct. 


## 4. 1st Start.

in time of first using You need to introduce yourself for be friendly with Git. It's little joke. Off course, Introducing is importante for the next time using this data in changes log *(Who, When, Why)*.

```
git config --global user.name "Your name"
git config --global user.email "Your email"
```

## <span style="color:green"> So, I cangradulate You with succeses in Git install. Go work! </span> 


## Basic commands in Git:
| Name | Git syntacsys | Description |
|:-------------|:-------------------|:---------------|
| Version | git version | for programm's version reviewing |
| Initialization | git init | for Git initialization with represitory|
| Status | git status | review current status of represitory|
| Change data | git add (file.*)| changing index to assign|
| Change fixation | git commit -m (message) | fix last changes and mark message|
| Error in commit message | git commit --amend -m *"comment"* | for change mistacke in commit message| 
| History | git log | history review for each changes|
| History | git log --oneline | short history review |
| Moving | git checkout | moving to another commits|
| Moving | git checkout master | move to back to Master active status|
| Comparing | git diff | review the privius commits with the last changing |



## 5. Repository initialization.
Repository is virtual storage for save versions of code. We can keep versions on server for same time work in one product.

Git comand: 
```
git init
```
This comand need to do one time for 1st repository installation (initialization). Same time will be created main branch (default name is **master** that we will study little below).


## 6. Changes fixation to repository.

All changes in Git fixing by **commits**.

Commits should tell a story of the history of your repository and how it came to be the way that it currently is. Commits include lots of metadata in addition to the contents and message, like the author, timestamp, and more.

Git comand: 
```
git status
git add <name>
git commit -m "changes description"
```

for make *commit* need to check status and add new changes to next time fixation (commit).

| Name | Git syntacsys | Description |
|:-------------|:-------------------|:---------------|
| Add data | git add (Repo_name) | add last changes to next step fixation |
| Fix | git commit -m "text" | make commit with message|
| Changes review | git log | for review all commits with messages of changes |
| Add + Commit | git commit -am "text" | for add and fix all last changes |
| If mistacke | git commit --amend "text" | for change message of the last commit |
| Moving between commits | git checkout (commit code) | for move to Code_commit (each commit has special code, as we can see after doing *git log* command)


As simple: Commit is fixation of changes with detail Who, When, Why.

## 7. Review history of commits.
```
git log
```
For review commits history, we are using *git log* command. 

| Name | Git syntacsys | Description |
|:-------------|:-------------------|:---------------|
| history review | git log | fulll list with commits|
| short history | git log --oneline | By default, it displays only the commit ID and the first line of the commit message. |
|log by Author | git shortlog |It groups each commit by author and displays the first line of each commit message. This is an easy way to see who’s been working on what|


## 8. Move between commits.

```
git checkout <commit_tag_name>
```

> When you have found a commit reference to the point in history you want to visit, you can utilize the git checkout command to visit that commit. Git checkout is an easy way to “load” any of these saved snapshots onto your development machine. /original description on the  [web-site](https://www.atlassian.com/git/tutorials/undoing-changes)/

Once you’re back in the main commit, you can use either *git revert* or *git reset* to undo any undesired changes.

## 9. Git ignore.

__gitignore__ - Specifies intentionally untracked files to ignore.
For excluding some files or folders from repositories viewing, we need to create special file **_.gitignore_**. And fix file_names or templates in accordance with have files or folders. 

## 10. Branches creation in Git.
![logo](git_branch.png)

Branch in Git - simple moving pointer to the one from commit, as usual last from saved in chain.
Default name of main branch is *'*master'*.

Main comands list for working with Branch:
| Name | Git syntacsys | Description |
|:-------------|:-------------------|:---------------|
| branch | git branch <branch_name> | new branch creation |
| branches list | git branch  | review full list of active branches |
| delete| git branch -d <branch_name>  | delete branch after completion of merge from additional branch to main|
| move data |  git merge <<branche_name>> | move data from <<branche_name>> branch to active branch|
| moving | branch checkout <brance_name> | for moving between branches

for example:
```
> git branch /total branches list review and check *active branch/
> git branch Template / new branch created with Template name/
> git checkout Template /moving from Master branch to Template/
> git checkout master /after working in the Template branche, move to the master/
> git merge Template /copy data from Teplate to master branch (should be active)/
> git branch -d Template /delete Template branche after finish merge comand/

```

as additional you need know *git checkout -b branche_name* comand - are using for one time action: create new branch and move to new branch.


## 11. Merge branches and conflicts fixation
For merge of selected branch with active branche(you can check active branch name with command *'git branch'*) need write below comand in terminal:;
```
git merge <branch_name>
```

If changed applied in the same position from other branches (as we try to merg), VS Code inform us proposed solutions for conflictes to solve.

Conflict place will be marked by 
*<<<<<<<, ======= and >>>>>>>*.

As usual, data before ======= refers to the host branch, after to the for were applied merge command. 

After your determinate some conflict, you need make correct activity for decided.

Git will inform you about conflicts in time and before merge completed. For review conflict text in detail we can do *git status* comand.
For resolve a conflicts as simple we can make it manually.
Also VS Code will propose actions for solve the conflict. You can choose and apply something if you want. 

**Don't forget about main comands of Git after merges completion**:
```
git status / git log / git add / git commit
```
After success of merge, we can delete the branch. We can use below commands:
```
git branch -d <branch_name>
git branch -D <branch_name>
```
Index -d (delete) possible to use if merge already completed with main branch. 

Iption -D meaning --delete --force and branch will be deleted not occour with merge status.  

You will see Error message in Terminal if try to delete not merged branch. Need to check current active branch and progresse merge.  
If you try to delete avtive branch, error message also will show in Terminal. You need make *git checkout* to Master branch. Progressed merge. Make solution and confirm merges conflicts, and after - progress *git branch -d <branch_name>*. 

## So, make resume
* git branch /list review/
* git branch NewBranch /create new/
* git checkout NewBranch /move to the new/
* *fix working in NewBranch*
* git chekout Master /default main branch name/
* git merge NewBranch /copy from NewBranch to Master/
* git branch -d NewBranch

## 12. Remote repository

As final section in the Git Instruction for new-workers we will learn princip of Remote repositories. 
For our practic we will use GitHub ([web-site](https://github.com)). 
Please progress registration for next time authorization and remote working.
Next step is New Repository creation in you personal account. Copy https:// for created repository and continius to work in VS Code programm for clone created Repository to local PC and work. 
```
git clone <http://...>
```
I will not spend more time on the new local Repository and file creation process. But be carefull with folders and changes fixation. 
``` cd ```  - command for moving in folder.
So, back to the remote -> local clone of the repository. Important Rules: we should create NEW_Branch for work and fix our result. After that send to Author of our clone repository New_Branch!

| Name | Git syntacsys | Description |
|:-------------|:-------------------|:---------------|
| Clone | git clone <url-adress> | copy remote repository to local work|
 | Remote | git remote add *origin* < url-adress > | assign name *origin* to remote repo with < url-adress >|
 Pull | git pull | move/pull info from remote repository to local + merge |
 |Push | git push | send changed file from local to remote account |

 "Fork" in GitHub: we can make Fork for project (copy other-person project to our worklist), if we would like some propose to improve of the current project. 
 So, fork -> copy https:// -> clone to local -> NewFile -> NewBranch -> Push to GitHub -> PullRequest in GitHub for next time merge by Author of project.



## <span style="color:yellow"> Let's do each yourself!</span> 


### Thank you!

### Have a nice day!


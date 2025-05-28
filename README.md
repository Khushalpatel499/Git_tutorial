# Git_tutorial
## master vs main:
    1. the terms master and main refer to the default branch name in a Git repository.
    2. master	The original default branch in Git	Used in older Git and GitHub versions.
    3. main	The new default branch name	Introduced in 2020 as the standard.
    4. GitHub and other platforms moved from master → main to use more inclusive and neutral language.
    5. to set default branch name: git config --global init.defaultBranch main
    6. Now, any time you run git init, the default branch will be main.
    7. Converting an existing master to main :
        git branch -m master main
        git push -u origin main
        git push origin --delete master
    8. -m stands for "move" (rename)
    9. -u sets tracking — this links your local main to the remote main 
        So future git push and git pull commands will know which remote branch to use

## Git-
    1. It is basically a version control system which track changes in code. 
    2. main features: a. track the histroy of code.
                      b. collaborate  
    3. Change in project is two ways in git: 1.add 2.commit  
    4.Git work on system for setup we required: a. A code editor 
                                                b. Window(GitBash) or Mac(Terminal)
    5. git --version : for check the version of git on system.
    6. ls  : differnt directories(files) present.
    7. clear : to clear gitbash.
    8. pwd : working directory(folder).
    9. ~ : show to we are in our main or root directory or primary folder.
    10. Git configure: a.It tell git on which account we are going to commit changes.
                       b.Two types: 1.global 2.local(if you have more than one git account).
                       c. git config --global user.name"githubAccountName"
                       d. git config --global user.email"someone@gmail.com"
                       e. git config --list: to see what we set 
    11. Two Place for changes : 1.remote(ex: github) 2. local(laptop,PC).
    12. Clone -a.To copy any repo form remote to local system.
               b.git clone <--some link-->

   
    13. cd- change directory which is of two type 
            a. go inside - cd foldername
            b. come outside - cd..  or cd\ -come to main directory
    14. ls -a : to see all files.
    15. Status: display state of code.(git status)
    16. When we have modifiy our file we have to do two step process add and commit.
    17.In git staturs we have 4 types files: a. untracked : new file that git doesn't track
                                             b. modified  : changed in file
                                             c. staged    : file is ready to commit means when any file is modified or untracked file add then we have to add that file that is staged then after we commit.
                                             d. unmodified: no change in file
    18. add :add new or changed file in working directory to the git area to known by git about them.
              command: git add . or git add <--file name-->
    19. commit: it is record of change we have done.
               command: gir commit -m"some message"
    20. All the add and commit which we have done is not show on github, it only available on local system so it only show how much commit we are ahead .
    21. To deal git with github the new push and pull command come.
    22.push : upload local repo to remote repo
             command : git push origin main
    23.General workflow:  make repo on github-> clone to local system -> make change-> add-> commit-> push.
    24. a.The above method is ok but let suppose already had made a project but now we want to push on github so we have to copy and paste the files into clone repo in general flow.
        b. So here come int command in picture to connect git.
        commands: 1.1 first make that git repo by : git init
                  1.2 and then make repo on github without readmefile because if we made then we can't push because system not have that file.
                  1.3 now we connect github repo and local repo which is now github repo by git init which add .git hidden file so command is:
                        git remote add origin <--github repo link-->
                  1.4 To verify that remote : git remote -v
                  1.5 to checke branch: git branch  (branch: it is bascially copy of project on which differnt team work under any project)
                  1.6 to rename brach : git branch -M main
                  1.7 then now git push origin main 
                  1.8 we can used above command as git push -u origin main because -u is setupstream which set origin main for whole project so now we have to write only git push command.
    25. Git branch : work on differnt brach of any project when work on large project and after working on separate branches we have to merge the branches or in general we have to make same code in both branch.
                     a. to create new branch: git checkout -b brachname
                     b. to go in differnt branch: git checkout branchname(where we want to go)
                     c. if we want to delete any branch: git brach id brachname


    26.Merge: Two ways: 1.to compare commit,branch,files: git diff <--branchname--> 
                          for merge:             git merge <--branchname-->
                        2.using git hub by creating PR(pull Request)
    27.Pull Request:tell others about change you have  pushed in a brach.
    28.pull: remote changes into local system
               command: git pull origin main
    29.merge conflict: when we merge two branches and  git does not know branch change put in main file.
    30. git log: to check all commit
    31. Undoing changes: When we change file but we want to go  back.
                      a. staged change(only add):
                              git reset <--filename> or git reset
                      b. commited changes(for one commit)
                            git reset HEAD~1
                      c. commited changes (for many commit):
                            copy the hash of that commit and then
                            git reset <--commit hash-->
                            if we want to remove change git as well as from code editor than
                            git reset --hard <-commit hash-->
    32.fork: it is a rough copy(make a copy of other project to other github account then we update the code and create pull request to the original account).
                         

    
    
    
## Github-
    1. A website that allow developers to store and manage their code.
    2. We can upload different repository(repo or folder) on github.  
    3. README.md(readme markdown): We can store the detail about project.
    4. Commit: change we made in our repo which increase the commit each time.
    
## Congfigure:
    1.if you want to use multiple git account then go to the particular repo cd /path/to/repo.
    2. set configure:     git config user.name "Your Name"                   git config user.email "your-email@example.com"
    3. check the path of the git repo command: git rev-parse --show-toplevel
    4. to see git remote url where it is pushing or pulling from command : git remote -v
    5. to see source of  each git config command: git config --list --show-origin
       ex: (.git/config = local, .gitconfig = global)

## local folder on github or gitlab:
    1. create a repo on github or gitlab without readme file and copy the http url.
    2. go to working local repo in git bash or terminal git intialize using command : git init
    3. then use git add and  git commit  command.
    4. now to add remote use: git remote add  origin url .
    5. and then push on : git push -u origin main
    6. work done you repo visible on github.
    7. if i made the readme file then the repo is not empty and in this case above method cause conflict.
    8. because both branch is diverged means suppose there are change in main branch and that changes are not in my branch and i want to push the change in the main branch so this called divereged and cause conflict.
    9. to solve this first pull the remote changes and then push command :git pull origin main --allow-unrelated-histories.
    10. if you are 100% sure that your local changes overwirte the remote changes then command: git push origin main --force
    11. to push if i create already a readme file:
            method1: a. clone the repo
                b. move local file into clone folder: cp -r /path/to/your/local-project/* repo-name/
                c. cd repo-name
                   git add .
                   git commit -m "Add local project files"
                   git push origin main
    12. method2: a. go to local folder : cd /path/to/your/local-project
                 b. initialized git ( to tell it is git repo): git init
                 c. set your local config if you want else global will consider : git config user.name "Your Name"      git config user.email "your@email.com"
                 d. add files:       git add .             git commit -m "Initial local commit"
                 e. add git remote url of repo: git remote add origin https://github.com/yourusername/repo-name.git
                 f. now to solve merge conflict pull to get readme file:  git pull origin main --allow-unrelated-histories
                 g. This downloads the README.md and merges it with our local files.
                 h. If there's a merge conflict, Git will tell you. You'll need to:
                        Open the conflicted file (usually README.md), 
                        Remove the conflict markers (<<<<<<<, =======, >>>>>>>),
                        Save it, and run:
                 i. git add README.md
                    git commit -m "Merge remote README with local files"
                 j.  now push command : git push origin main
                 k.  now local and remote repo are combined and sync.


                



    

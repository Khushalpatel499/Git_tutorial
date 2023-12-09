# Git_tutorial
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

   
=======
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

=======
    26.Merge: Two ways: 1.to compare commit,branch,files: git diff <--branchname--> 
                          for merge:             git merge <--branchname-->
                        2.using git hub by creating PR(pull Request)
    27.Pull Request:tell others about change you have  pushed in a brach.
    28.pull: remote changes into local system
               command: git pull origin main

    
    
    
## Github-
    1. A website that allow developers to store and manage their code.
    2. We can upload different repository(repo or folder) on github.  
    3. README.md(readme markdown): We can store the detail about project.
    4. Commit: change we made in our repo which increase the commit each time.
    
    

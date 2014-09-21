
This document provides simple instruction for setting up and syncing repositories on Mac OS computers and GitHub, and for linking RStudio project repositories with GitHub. It assumes that you have a GitHub account, have installed Git on your local computer, and have configured Git with your GitHub username and email address. 

1.  Create repo on GitHub, clone to local computer, and sync

    - Add a new repo to GitHub using **+** at the top of your user page
    - When the repo is created, copy the **HTTPS clone URL** (bottom right)
    - Go to local computer, open Terminal and cd to directory where you want the local repo to be placed
    - enter: 
        - git clone 'https://github.com/\<username\>/\<reponame\>.git'
            - \<username\> is your GitHub username and \<reponame\> is the name of the repo you just created
    - Add files to the local \<reponame\> directory that you would like to commit
    - to stage files for commit enter:
        - git add .
    - to commit enter: 
        - git commit -m "commit message"
            - commit message is the message you want to attach to the commit
    - to sync with GitHub enter:
        - git push -u origin master
        
2. Set up version control for an existing RStudio project, create a GitHub repo, and sycn RStudio with GitHub

    - Basic instruction for using Git with RStudio Version Control can be found at: https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN?version=0.98.1028&mode=desktop
    - Create a local Git repository for your RStudio project using the Tools > Version Control > Project Setup menu
    - Stage files for commit from within RStudio **Git** tab (top right)
    - Commit files and add commit message
    - In GitHub, create new repository for this project
        - ***Do Not*** select **Inititalize the repository with a README**
            - The README file will cause problems with syncing
    - Open Terminal in local computer, cd to directory containing R project
    - enter:
        - git remote add origin https://github.com/<username\>/<reponame\>.git
            - \<username\> is your GitHub username and \<reponame\> is the name of the repo you created in GitHub
    - to sync enter:
        - git push -u origin master
    - subsequent syncs after additional commits can be initiated with the **Push** button of the RStudio **Git** tab    
        
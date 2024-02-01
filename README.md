# Git and Github 
Git is the free and open-source distributed version control system that's responsible for everything GitHub-related that happens locally on your computer
  1. Git is a version control system.
  2. Git helps you keep track of code changes.
  3. Git is used to collaborate on code.

# What does Git do?
  1. Manage projects with Repositories
  2. Clone a project to work on a local copy
  3. Control and track changes with Staging and Committing
  4. Branch and Merge to allow for work on different parts and versions of a project
  5. Pull the latest version of the project to a local copy
  6. Push local updates to the main project

# Working with Git
  1. Initialize Git on a folder, making it a Repository
  2. Git now creates a hidden folder to keep track of changes in that folder
  3. When a file is changed, added or deleted, it is considered modified
  4. You select the modified files you want to Stage
  5. The Staged files are Committed, which prompts Git to store a permanent snapshot of the files
  6. Git allows you to see the full history of every commit.
  7. You can revert to any previous commit.
  8. Git does not store a separate copy of every file in every commit, but keeps track of changes made in each commit!

# Frequently used Git Command
  1. # SETUP - Configuring user information used across all local repositories
      ## 1. Set a name that is identifiable for credit when reviewing version history
          git config --global user.name “[firstname lastname]”
      ## 2. Set an email address that will be associated with each history marker
          git config --global user.email “[valid-email]”
      ## 3. Set automatic command line coloring for Git for easy reviewing
          git config --global color.ui auto

  2. # SETUP & INIT - Configuring user information, initializing and cloning repositories
      ## 1. initialize an existing directory as a Git repository
         git init
      ## 2. Retrieve an entire repository from a hosted location via URL
         git clone <URL>
     
  3. # STAGE & SNAPSHOT - Working with snapshots and the Git staging area 
      ## 1. Show modified files in the working directory, stage for your next commit
          git status
      ## 2. Add a file as it looks now to your next commit (stage)
          git add [file]
      ## 3. Unstage a file while retaining the changes in the working directory
          git reset [file]
      ## 4. diff of what is changed but not staged
          git diff
      ## 5. diff of what is staged but not yet committed
          git diff --staged
      ## 6. Commit your staged content as a new commit snapshot
          git commit -m “[descriptive message]”
     
   5. # BRANCH & MERGE - Isolating work in branches, changing context, and integrating changes
      ## 1. List your branches. a * will appear next to the currently active branch
          git branch
      ## 2. Create a new branch at the current commit
          git branch <branch name>
      ## 3. Switch to another branch and check it out in your working directory
          git checkout <branch name>
      ## 4. Merge the specified branch’s history into the current one
          git merge <branch name to be merged from the main branch>
      ## 5. diff of what is staged but not yet committed
          git diff --staged
      ## 6. Show all commits in the current branch’s history
          git log

   6. # SHARE & UPDATE - Retrieving updates from another repository and updating local repos
      ## 1. Add a git URL as an alias
          git remote add [alias] [url]
      ## 2. Fetch down all the branches from that Git remote
          git fetch <alias>
      ## 3. Merge a remote branch into your current branch to bring it up to date
          git merge [alias]/[branch]
      ## 4. Transmit local branch commits to the remote repository branch
          git push <alias> <branch>
      ## 5. fetch and merge any commits from the tracking remote branch
          git pull 
      ## 6. Show all commits in the current branch’s history
          git log

  6. # TEMPORARY COMMITS - Temporarily store modified, tracked files to change branches
      ## 1. Save modified and staged changes
          git stash
      ## 2. Write working from the top of the stash stack
          git stash pop
      ## 3. Merge a remote branch into your current branch to bring it up to date
          git merge [alias]/[branch]
      ## 4. Delete the stash changes 
          git stash clear

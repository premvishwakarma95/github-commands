# github-commands
- Learn all about git docs from below link by hitesh
- https://docs.chaicode.com/youtube/chai-aur-git/welcome/

## What is Git?
- Git is software.
- Git is a version control system.
- It helps developers track changes in their code over time.
- Think of Git like a time machine for your code ⏳
- With Git, you can:
- Track who changed what and when
- Go back to previous versions of code
- Work on new features safely using branches
- Merge code from multiple developers without conflicts (or handle them properly)
- 👉 Git works locally on your computer.

---

## What is github?
- GitHub is a cloud-based platform that hosts Git repositories.
- Think of GitHub as Google Drive for Git projects ☁️
- With GitHub, you can:
- Store your Git repositories online
- Share code with others
- Collaborate with teams
- Review code using Pull Requests
- Track issues and bugs
- Deploy projects
- 👉 GitHub is remote, Git is local.

| Feature       | Git             | GitHub                       |
| ------------- | --------------- | ---------------------------- |
| Type          | Tool            | Platform                     |
| Works Offline | ✅ Yes           | ❌ No                         |
| Purpose       | Version control | Code hosting & collaboration |
| Owned by      | Open-source     | Microsoft                    |

---

## How to take access of a repo with the help of classic github token?
- Run this below command in git bash so it will not only give the code it will give access of that branch and account so you can run commands like push, pull, commit etc.
- git clone https://ghp_SWK4EKA8T1PIjhfghfghhgfhfghGWf@github.com/premvishwakarma95/active-aurora-admin-main.git

---

## Common commands
```bash
git --version
git status // this tell us, Is there anything changed in our current repo and .git file should present only then this command work
git clone https://github.com/username/repo-name.git
git clone https://ghp_SWK4EKA8T1PIjhfghfghhgfhfghGWf@github.com/premvishwakarma95/active-aurora-admin-main.git
git status
git add .
git commit -m "Initial commit"
git push origin main
git pull origin main
```

---

## Git config commands
We use these Git config commands to identify who you are when you make commits 👤
```bash
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"
// This will show you all the settings that you have changed.
git config --list
```

---

## Creating a repository
```bash
git init
git add <file> <file2>     // this will add only file1 and file2 changes
git add .                 // this will add all the changes of all file
git status
git commit -m "commit message"
git status
git push origin prem_dev
```

## Logs
This command will show you the history of your repository. It will show you all the commits that were made to the repository. You can use the --oneline flag to show only the commit message. This will make the output more compact and easier to read.
```bash
git log
```

---

## .gitignore
Now, when you run the git status command, it will not show the node_modules and .vscode folders as being tracked by git.
- .gitignore
```bash
node_modules
.env
.vscode
```

---

## .gitkeep
- git doesn't add empty folder and if we want to add that folder in repo at that time we use .gitkeep file.
- we need to define .gitkeep inside empty folder that we want to keep in repo
- empty_folder/.gitkeep

---

## Creating a new branch
- IF you have initialized git and now want to create branch then you won't be able to create branch because first atleast we need to do one commit to master or main branch only then we can create new branch and only then you can run git branch..
- To create a new branch, you can use the following command:
```bash
git branch                     // this command will tell all the branches that are present in the repository.
git branch --show-current      // this will tell the current branch that you are in.
git branch bug-fix             // this command will create bug-fix branch but your current branch will still be master i mean you would be still in current branch where you were.
git switch bug-fix             // this command will switch from one branch to another i mean if we are in "master" branch right now and want to go in bug-fix branch then we use this command.
git log                        // this will give all the logs of git activity.
git switch main
git switch -c dark-mode        // this will create a new branch with name dark-mode and now you will be in dark-mode branch i mean your current branch would be this.
git checkout orange-mode       // this will switch from current master branch to orange-mode branch if this branch exists.
git checkout -b ligth-mode     // this will create new branch and make current branch light-mode, now you will work on this light-mode branch.
```

---

## Delete a branch
You can delete a branch using the following command:
```bash
git branch -d <branch-name>
```

---

## Rename a branch
You can rename a branch using the following command:
```bash
git branch -m <old-branch-name> <new-branch-name>
```

## Merging branches
- Merging is about bringing changes from one branch to another.
- In Git we have two types of merges :
- - Fast-Forward Merges (If branches have not diverged)
- - 3-Way Merges (if branches have diverged)

### Fast forware merge
- First go to in that branch in which you want to take changes from another branch using this "git checkout main" command.
- Now run this second command "git merge bug-fix" this will take code from bug-fix to main branch
- this is called fast forward merge.
```bash
git checkout main
git merge bug-fix
```

### command to abort merge
```bash
git merge --abort
```

---

### What is `git diff`?
- `git diff` shows the difference between your working code and the last committed version.
- It tells you what you have changed but not yet added (staged).
```bash
git diff
```

---

### What is `git diff --staged`?
- `git diff --staged` shows the changes that are already added to the staging area and will be included in the next commit.
- I mean to say this command shows what changes we have last committed or added.
- Simple example -> Step 1: Edit a file
```js
const version = 1;
```
- Change it to:
```js
const version = 2;
```
Now if we will run `git diff --staged` then we will get this below thing.
```diff
- const version = 1;
+ const version = 2;
```

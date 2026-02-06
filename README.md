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
git add <file> <file2>
git status
git commit -m "commit message"
git status
```

## Logs
This command will show you the history of your repository. It will show you all the commits that were made to the repository. You can use the --oneline flag to show only the commit message. This will make the output more compact and easier to read.
```bash
git log
```


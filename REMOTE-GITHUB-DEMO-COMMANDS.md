# Remote GitHub Demo Commands

Use this file during Lecture 1 to demonstrate the remote GitHub workflow.

## 1. Start locally

```powershell
git status
git log --oneline
```

## 2. Create an empty repository on GitHub

Recommended name:

`lecture-01-github-remote-demo`

Do not initialize it with a README if you want the cleanest first push demo.

## 3. Connect local repo to GitHub

Replace the username below with your own GitHub username.

```powershell
git branch -M main
git remote add origin https://github.com/<your-github-username>/lecture-01-github-remote-demo.git
git remote -v
git push -u origin main
```

## 4. Create a feature branch live in class

```powershell
git switch -c feature/class-notes
Add-Content .\notes\session-summary.md "`n- Branch demo note added during class"
git status
git add .
git commit -m "Add class branch note"
git push -u origin feature/class-notes
```

## 5. Demo clone and pull

```powershell
git clone https://github.com/<your-github-username>/lecture-01-github-remote-demo.git
git pull origin main
```

## Important points to note

Explain this sequence clearly:

1. Local repo is created on your machine.
2. Remote repo lives on GitHub.
3. `git remote add origin` connects the two.
4. `git push` sends local commits to GitHub.
5. `git clone` copies the remote repo onto another machine.
6. `git pull` brings newer remote changes back to local.

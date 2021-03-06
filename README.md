### Git CLI
```
sudo apt install git-all

git version

git config --global user.name <USERNAME>
git config --global user.email <EMAIL>

// store or cache GitHub credentials
git config --global credential.helper store
-OR-
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=28800'

git config --list

git clone https://github.com/gdmoney/Git.git

git show
git status

git fetch
git pull
git commit -am <COMMENT>
git push

git add <FILENAME>

// discard changes in working directory
git restore <FILENAME>

// undo changes made in the last commit
git revert HEAD
git push

// change local repo name after changing it on GH
git remote -v
git remote set-url origin https://github.com/gdmoney/NEW-NAME
git remote -v
git pull

// delete a file with sensitive data from all commits
git filter-branch --force --index-filter \
  "git rm --cached --ignore-unmatch PATH_TO_FILE_TO_DELETE" \
  --prune-empty --tag-name-filter cat -- --all
git push origin --force --all
```

### GitHub CLI
```
gh version

gh auth login
gh auth status

gh config set git_protocol [SSH or HTTPS]
gh config get git_protocol

gh repo clone gdmoney/Git

gh workflow list
gh workflow run WORKFLOW_NAME.yml

gh run list --workflow=WORKFLOW_NAME.yml
gh run view
gh run watch
```

**Upgrade:**
- Linux: 
```
sudo apt update
sudo apt upgrade gh
```

- Windows:
  - run cmd as admin
```
choco upgrade gh
```

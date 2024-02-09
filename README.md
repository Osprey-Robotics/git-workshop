# UNF Git Workshop

This is a sample readme and repo for demonstration and learning basic git
commands and some best practices. The contents are not important.

Below is the list of commands run, give or take

## init repo
```bash
mkdir git-workshop
cd git-workshop/
git init .
ls -la
git status
cp ../git-workshop-prep/LICENSE.txt ./
git status
git add LICENSE.txt
git commit
cp ../git-workshop-prep/README.md ./
git add README.md
git commit README.md
git tag init-repo
git remote add origin git@github.com:Osprey-Robotics/git-workshop.git
git push --set-upstream origin master
git push --tags
```

## working with files
```bash
cp ../git-workshop-prep/ozzie.cpp ./
g++ ozzie.cpp
ls -l
git status
git add .
git status
git reset
git status
nano .gitignore
git status
git add .gitignore
git commit .gitignore
git add ozzie.cpp
git commit ozzie.cpp
git status
cp ../git-workshop-prep/*py ./
python ozzie.py
ls -l
git status
nano .gitignore
git commit .gitignore
mkdir src
git mv duuuvaall.py src/
git status
git commit
git mv ozzie.py src/
git status
git commit
git tag working-with-files
```

## modify, readd, amend
```bash
nano ozzie.py
git diff
git add ozzie.py
git diff
nano ozzie.py
git diff
git status
git commit ozzie.py
git status
git diff
git add ozzie.py
git commit --amend
nano ozzie.py
git commit --amend --no-edit
git tag modify-readd-amend
git push --tags
```

## reset soft/hard, rebase/
```bash
cp ../git-workshop-prep/*png ./
tyls im-a-binary-dont-commit-me.png
git status
git add im-a-binary-dont-commit-me.png
git commit im-a-binary-dont-commit-me.png
git reset HEAD~1
git status
git commit im-a-binary-dont-commit-me.png
git reset HEAD^1
git status
git rebase -i --committer-date-is-author-date HEAD~5
ls -l
git tag reset-soft-hard-rebase
```

## branch/pr/pull
```bash
git branch new-feature
git checkout new-feature
nano src/ozzie.py
git add ozzie.py
git commit ozzie.py
git checkout master
git merge master new-feature
git branch hacker-back-door
git checkout hacker-back-door
nano src/ozzie.py
git add ozzie.py
git commit ozzie.py
git checkout master
git push -u origin hacker-back-door
git pull
```

## github actions
```bash
cp -r ../git-workshop-prep/.github/ ./
ls -la
nano .github/workflows/main.yml
git add .github/workflows/main.yml
git commit
nano ozzie.py
git add ozzie.py
git commit ozzie.py
git push
```

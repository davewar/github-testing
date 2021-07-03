# GITHUB CHEATSHEET FOR MARKDOWN

https://www.markdownguide.org/cheat-sheet

---

git status \*\* what branch and status of files

git branch alpha \*\*CREATE BRANCH named alpa

git branch --list \*\* info - lists all branches. The '\*' tells which branch
you are on.

git branch \*\* info - lists all branches. The '\*' tells which branch you are
on.

git checkout alpa \*\*To switch to the 'alpa' branch

git checkout main \*\*To switch to the 'main' branch

`` git checkout -b beta \*\* This commands CREATE BRANCH named 'beta and also
switches to that branch

`` if your on branch beta - you can compare beta to say the main branch git diff
main

``

After creating the branches - add the branch to the github website by

- git push --set-upstream origin alpa
- git push --set-upstream origin beta

To move your alpa changes to the main branch.

1. git chekout main
2. git merge alpa
3. git push

To Delete the alpa branch as no longer required.

1. git branch -d alpa
2. git push origin :alpa

if you made changes on beta branch and your main branch had changed since as
well

1. git commit + push the changes on the beta branch
2. git checkout main
3. git merge beta

A message will advise if a conflcts exist – it yes, it will advise

head = main

```<<<<<<< HEAD <p>This is a new para</p> <p>This is aa new para</p> <p>This is
aaa new para</p> <p>This is aaaa new para</p> ======= <p>this is a beta para</p>

<h2>This is a H2</h2> <h1>This is a h1</h1>

> > > > > > > beta

```

You can edit directly in the screen – I changed to the below

```

   <div className='App'>

            <p>This is a new para</p>

            <p>this is a beta para</p>
            <h2>This is a H2</h2>
            <h1>This is a h1</h1>

        </div>

```

4. save changes on this main branch and then add > commit > push

**To restore to last commit**

1)git reset ee44e82 (the last saved change) 2) git restore src/App.css (name of
file)

## if you dont want to push after commit

git reset head~1 or git reset src/App.css (name of file)

## if you want to restore file before commit.

git restore src/App.css

## if i commited and not pushed a change. if someone else was to add a new file. if I was then to push, I would get error, to say that I have missing changes. To fix, I would have to pull the new additions.

git pull and then if no issues you would git push

## if i were working on a branch or main and someone created a new branch with a file I dont have. In order to get this file, I would need to fetch it

- git fetch origin
- git checkout nameofnewbranch

```

```

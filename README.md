# GITHUB CHEATSHEET

Commands: https://education.github.com/git-cheat-sheet-education.pdf

Markdown: https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf

- git commit -am "."
- git push

---

`git status` - what branch and status of files

`git branch alpha` - CREATE BRANCH named alpa

`git branch --list` - lists all branches. The '\*' tells which branch you are
on.

`git branch` - lists all branches. The '\*' tells which branch you are on.

`git checkout alpa` - To switch to the 'alpa' branch

`git checkout main` - To switch to the 'main' branch

`git checkout -b beta` - This commands CREATE BRANCH named 'beta and also
switches to that branch

`git diff main` - if your on branch beta - you can compare beta to say the main
branch

**After creating the branches - add the branch to the github website by**

- git push --set-upstream origin alpa
- git push --set-upstream origin beta

**To move your alpa changes to the main branch.**

1. git chekout main
2. git merge alpa
3. git push

**To Delete the alpa branch as no longer required.**

1. git branch -d alpa
2. git push origin :alpa

**If you made changes on beta branch and your main branch had changed since as
well**

1. git commit + push the changes on the beta branch
2. git checkout main
3. git merge beta

If a conflcts exist, then you will be advised e.g

```
<<<<<<< HEAD
<p>This is a new para</p>
<p>This is aa new para</p>
 <p>This is aaa new para</p>
 <p>This is aaaa new para</p>
  ======= <p>this is a beta para</p>

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

**If you did a change and pushed it. if your boss said reverse it afterwards**

- use `git revert ee44e82` => `:wq` => `git push` (enter the commit ref you did)
  and this will revert back to the original status\*\*

**If you did a change and pushed it. if your boss said reverse it afterwards**

- use `git revert HEAD~1` => `:wq` => `git push` (enter the commit ref you did)
  and this will revert back to the original status\*\*

**If you dont want to push after commit**

-`git reset head^1` or `git reset head~1` or `git reset src/App.css` (name of
file).

**If you want to restore file before commit.**

- `git restore src/App.css`

**If i commited and not pushed a change. if someone else was to add a new file.
if I was then to push, I would get error, to say that I have missing changes. To
fix, I would have to pull the new additions.**

- `git pull` and then if no issues you would git push

**If i were working on a branch or main and someone created a new branch with a
file I dont have. In order to get this file, I would need to fetch it.**

- `git fetch origin`
- `git checkout nameofnewbranch`

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

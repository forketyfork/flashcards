START
Basic
Front: How do you squash your branch to a single commit?
Back: 
```sh
git switch yourBranch
git reset --soft $(git merge-base master HEAD)
git commit -m "one commit on yourBranch"
```
<!--ID: 1745138945661-->
END

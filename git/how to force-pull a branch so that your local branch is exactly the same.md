START
Basic
Front: How to force-pull a branch, so that your local branch commits are discarded, and your local branch is exactly the same as the remote branch?
Back: 
```shell
git fetch origin some-branch
git reset --hard origin/some-branch
```
<!--ID: 1745138945663-->
END

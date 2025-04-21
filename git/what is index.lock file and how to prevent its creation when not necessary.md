START
Basic
Front: 
What is `index.lock` file? How to make sure git doesn't create it when not necessary?
Back: 
`index.lock` is located in the `.git` folder. It's a lock file created by git when it touches the index during some operations. It also happens during a simple `git status` execution. 

If it causes trouble (e.g., when git is executed in parallel), you can run git with the `--no-optional-locks` parameter (`git --no-optional-locks status`) or by setting the `GIT_OPTIONAL_LOCKS` environment variable to 0. Then git won't perform optional operations that require locks.
<!--ID: 1745138945654-->
END

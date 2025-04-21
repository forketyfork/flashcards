START
Basic
Front: How do you create a git patch and apply it to a different directory?
Back: 
Creating a git patch, e.g. comparing the current `HEAD` with the `master`:
`git diff master HEAD > patchfile`

Now cd to the proper directory and run the `patch` command:
`patch --strip 1 --batch --directory . --input patchfile`

The `--strip 1` (`-p`) argument will make sure to strip the `a/` from the beginning of the file names in git diff.
The `--batch` (`-t`) argument will enter batch mode, so it won't ask interactively how to apply patches to files that were not found.
The `--input` (`-i`) argument provides the file, which can also be provided as stdin using `< file.patch`.
<!--ID: 1745138945665-->
END

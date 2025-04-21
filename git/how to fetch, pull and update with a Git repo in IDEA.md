START
Basic
Front: How to fetch, update and pull branches or update the project in IDEA?
Back: 
- to fetch, select `Git -> Fetch` or open the `Branches` popup and click on a dashed arrow button in the upper right corner; this will only fetch the remote branches, not update the local ones;
- to update a local branch to the remote state, in the `Branches` popup or in the `Branches` pane of the `Version Control` tool window, select a branch and choose `Update` from the context menu; IDEA will pull the remote branch and rebase or merge it into the local branch, depending on the update method in `Settings -> Version Control -> Git`
- `Git -> Pull...` opens a Pull dialog that allows to pull any branch into your current branch. The changes will be merged. There are some additional `git pull` parameters in the dropdown.
- "Update project" (Cmd+T) action fetches all changes from the repository and updates the tracked branches using the update method specified in the settings; if you've hidden the settings window for this action, you can show it again by going to `Version Control -> Confirmation` tab and checking the "Show options before: Update" setting.
<!--ID: 1712155821790-->
END

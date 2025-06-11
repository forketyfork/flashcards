START
Basic
Front: 
What does `y` mean in `git add -p` interactive mode?
Back: 
Yes - stage this hunk
<!--ID: 1749631193366-->
END

START
Basic
Front: 
What does `n` mean in `git add -p` interactive mode?
Back: 
No - skip this hunk (don't stage it)
<!--ID: 1749631193367-->
END

START
Basic
Front: 
What does `s` mean in `git add -p` interactive mode?
Back: 
Split - break this hunk into smaller pieces
<!--ID: 1749631193368-->
END

START
Basic
Front: 
What does `q` mean in `git add -p` interactive mode?
Back: 
Quit the interactive session (keeps what you've staged so far)
<!--ID: 1749631193369-->
END

START
Basic
Front: 
What does `a` mean in `git add -p` interactive mode?
Back: 
Accept ALL remaining hunks (stage everything left)
<!--ID: 1749631193370-->
END

START
Basic
Front: 
What does `d` mean in `git add -p` interactive mode?
Back: 
Decline ALL remaining hunks (reject everything left)
<!--ID: 1749631193371-->
END

START
Basic
Front: 
What does `e` mean in `git add -p` interactive mode?
Back: 
Edit this hunk manually in your text editor
<!--ID: 1749631193372-->
END

START
Basic
Front: 
What does `j` mean in `git add -p` interactive mode?
Back: 
Jump to next hunk (navigation without making a decision)
<!--ID: 1749631193373-->
END

START
Basic
Front: 
What does `J` mean in `git add -p` interactive mode?
Back: 
Jump to next FILE
<!--ID: 1749631193374-->
END

START
Basic
Front: 
What does `p` mean in `git add -p` interactive mode?
Back: 
Print/show the current hunk again
<!--ID: 1749631193375-->
END

START
Basic
Front: 
What are the 3 most commonly used options in `git add -p`?
Back: 
`y` (yes), `n` (no), and `s` (split)
<!--ID: 1749631193376-->
END

START
Basic
Front: 
When would you use the `s` option in `git add -p`?
Back: 
When a hunk is too big and you only want to stage part of it - splits it into smaller pieces
<!--ID: 1749631193377-->
END

START
Basic
Front: 
What git command starts interactive staging to selectively add changes?
Back: 
`git add -p`
<!--ID: 1749631193378-->
END

START
Basic
Front: 
What's a good workflow for moving some changes from one branch to a new branch?
Back: 
1. `git stash` your changes
2. `git checkout -b new-branch`  
3. `git stash apply`
4. Use `git add -p` to selectively stage what belongs on this branch
5. Commit, then switch back and repeat for remaining changes
<!--ID: 1749631193379-->
END
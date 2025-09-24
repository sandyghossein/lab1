Git answers:


Exercise 1:

3.a. The .git directory stores repository metadata and object database(commits,ref,config)

6.a. The file appears in staging area(changes to be commited).

11.git diff shows no output because diff compares working tree vs HEAD.

     To see diff of staged changes: git diff --staged
   
12. When you git add again, latest changes move into the staging area.
     We commit to record them: git commit -m "Update file1"
    
14.a. The first seven characters are usually enough.

Exercise 2:

1.git status shows current branch (master).

5.git log shows recent commits on that branch.

8.a. no merge commit, history is linear.

Exercise 3:

6.b. The changes from step 5 are discarded (lost from working tree).

6.c. git restore file3.py

8.a. git revert creates a new commit that undoes the changes (history preserved).

10.a. This moves HEAD back but keeps changes staged.

10.b. The commit is removed from branch tip (history moved), but changes remain in staging area.

11.a.Unstages files (moves staged changes to working directory).

11.b. Using HEAD means reset index to HEAD 

12.a. Resets working directory and staging area to HEAD; discards changes.

12.b. Default target is HEAD when no commit provided.

12.c. If done right after step 9, you'd lose the uncommitted changes.

Exercise 4:

6.a. Rebase reapplies feature-branch commits on top of master, master is the base.

6.c. Difference from merge: rebase rewrites history (no merge commit), producing a tidy linear history.

9.After rebase, use git log --oneline --graph --branches to inspect the new linear history.

11.b.Squashing takes two or more commits and merges them into a single commit.

The changes from all the squashed commits are included, but the history shows one commit instead of multiple.

11.d.This rewrites history by modifying old commits, which is useful for cleaning up mistakes or improving commit messages before sharing your branch.

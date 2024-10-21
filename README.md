# Static Website (HTML, CSS)

## This is a collaboration project for Xeniya and Ceyda.

# Usage (locally):

With Python on a command line:

```
python -m http.server
```

or in VS code:

Clone the repo. Open the folder in VS code, hit:

```
Go Live
```

## Contributing

1. Create a branch
2. Commit changes
3. Push to origin git push `--set-upstream origin curr-branch-name`
4. Make PR in GitHUb with a button
   4a. Reviewer: Look at the changes on Github
   4aa. If want to look locally: `git checkout -b myb origin/myb`, where `myb` is the name of the branch to review. After took a look, delete it locally
   4b. Reviewer: hit the approve button on GitHub
5. PR-Sender: Merge PR (squish)
6. Delete the branch in GH (make automatic)
7. Check out main, Pull main, delete branch `git branch -d branch-name`

## Merge Conflicts (caused localy) Handling

1. Start with a txt file with a list. Start on branch `main`
   2.3. Create a new branch `feature1`. Add an item to the end of a list & commit
2. Checkout same branch (`main`)
3. Add new branch `Feature2` (of `main`)
4. Add an item to txt. Commit
5. `git merge feature1`
   7a. abort the merge
   7b. Do the merge again and fix the conflict
6. Delete `feature1`
7. checkout `main` , merge `feature2` (stage,commit), delete `feature2`

## Merge Conflicts (collaborating online) Handling

1. user_peach creates a branch > eddit file > stage > commit > push > make PR
2. user_bunny creates a branch > eddits THE SAME line > stages > commit > push > make PR
3. user_peach merges PR > pull > cleanup branches
4. conflict is on GitHub (look at conflict message in there)
5. user_bunny `git pull origin main` (while still checked out on their branch)
6. user_bunny resolve conflict (VS code) > stage > commit > push
7. merge PR button active > cleanup branches

8. Note: When pulling origin/main to a local branch you might get an error about non-fast-forward changes. This might fix it: `git pull --no-ff origin main` (instead of git pull origin main)

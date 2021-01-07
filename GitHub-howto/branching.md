# Branching
A reminder of main commands for branching / how to use branch:

## Create a branch:
* List all existing branches:
    ```bash
    git branch -a
    ```
* Create a new branch:
    ```bash
    git branch a_new_branch
    ```
   A good practice is to include a reference to the issue (if any) this branch is addressing, e.g. ***b_issue1***

* Switch to the new branch:
    ```bash
    git checkout b_issue1
    ```

* Push the newly created branch to remote:
    ```bash
    git push -u origin b_issue1
    ```
    
    **-u** (equivallent to --set-upstream) is required first time the branch is pushed.

## Add/commit on a branch:
Same as on main, e.g. :
```bash
git add new_file_to_track
git commit -m 'my comment'
git push -u origin b_issue1
```

## Merge branch with main:
* First we need to checkout to main, then merge:

    ```bash
    git checkout main
    git merge b_issue1
    ```

* We can then delete the branch:

    ```bash
    git branch -d b_issue1
    ```
* And push the new main to remote:

    ```bash
    git push -u origin main
    ```


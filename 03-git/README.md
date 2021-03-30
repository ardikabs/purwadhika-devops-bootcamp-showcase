# GIT

## Topics
* GIT

## Showcase
1. Compare different between branch
    ```bash
    $ git log <target_a>..<target_b>
    ```
1. Override recent commit with newest commit
    ```bash
    $ git commit --amend -m <commit_msg>
    ```
1. Change commit author
    ```bash
    $ git commit --amend --reset-author -m <commit_msg>`
    ```
1. Reset to an old revision
    ```bash
    $ git reset --soft <previous_commit_sha>
    $ git reset --hard <previous_commit_sha>
    ```
1. Add recent files and/or old file into ignored files
    ```bash
    $ git rm --cached $(git ls-files --ignored --exclude-from=.gitignore)
    ```
1. Reset specific file to and old revision
    ```bash
    git checkout <commit_msg> -- <filename>
    ```
1. Temporary saving file before make any commit
    ```bash
    $ git stash -m <context_msg>
    $ git checkout <new_branch>
    $ git add .
    $ git commit -m <commit_msg>
    ```
1. Restructure commit history
    ```bash
    $ git rebase -i <target_commit>
    ```
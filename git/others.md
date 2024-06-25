# Git Commands

This document contains some of the more advanced git commands you need to know to work with git. If you are new to git, you can check the [basics](basics.md) document.

## Advanced Commands

### Branching

To create a new branch in your repository, run the command:

```bash
git checkout -b <branch_name>
```

To switch to an existing branch, run the command:

```bash
git checkout <branch_name>
```

To list all the branches in your repository, run the command:

```bash
git branch
```

To delete a branch, run the command:

```bash
git branch -d <branch_name>
```

### Merging

To merge a branch into the current branch, run the command:

```bash
git merge <branch_name>
```

### Rebasing

To rebase the current branch onto another branch, run the command:

```bash
git rebase <branch_name>
```

### Stashing

Stashing is used to save your changes temporarily without committing them.

To stash your changes, run the command:

```bash
git stash
```

To list all the stashes, run the command:

```bash
git stash list
```

To apply a stash, run the command:

```bash
git stash apply
```

To apply a specific stash, run the command:

```bash
git stash apply stash@{<stash_number>}
```

To delete a stash, run the command:

```bash
git stash drop
```

To delete a specific stash, run the command:

```bash
git stash drop stash@{<stash_number>}
```

### Tagging

Tags are used to mark a specific commit in your repository.

To create a tag, run the command:

```bash
git tag <tag_name>
```

To create an annotated tag, run the command:

```bash
git tag -a <tag_name> -m "Your tag message"
```

To list all the tags in your repository, run the command:

```bash
git tag
```

To push a tag to the remote repository, run the command:

```bash
git push origin <tag_name>
```

To push all the tags to the remote repository, run the command:

```bash
git push origin --tags
```

### Undoing Changes

To undo the changes in a file, run the command:

```bash
git checkout -- <file_name>
```

To undo the last commit, run the command:

```bash
git reset HEAD~1
```

To undo the last commit and keep the changes, run the command:

```bash
git reset HEAD~1 --soft
```

To undo the last commit and discard the changes, run the command:

```bash
git reset HEAD~1 --hard
```

To undo the last commit and keep the changes in the staging area, run the command:

```bash
git reset HEAD~1 --mixed
```

### Useful Commands

To see the changes in a file, run the command:

```bash
git diff <file_name>
```

To see the changes between two commits, run the command:

```bash
git diff <commit_id_1> <commit_id_2>
```

To see the changes in the staging area, run the command:

```bash
git diff --staged
```

To see the changes in the working directory, run the command:

```bash
git diff HEAD
```

To see the changes in a specific file between two commits, run the command:

```bash
git diff <commit_id_1> <commit_id_2> -- <file_name>
```

To see the changes in a specific file in the staging area, run the command:

```bash
git diff --staged -- <file_name>
```

To see the changes in a specific file in the working directory, run the command:

```bash
git diff HEAD -- <file_name>
```

To see the changes in a specific file between two commits in the staging area, run the command:

```bash
git diff --staged <commit_id_1> <commit_id_2> -- <file_name>
```

To see the changes in a specific file between two commits in the working directory, run the command:

```bash
git diff <commit_id_1> <commit_id_2> -- <file_name>
```

To see the changes in a specific file between two commits in the staging area, run the command:

```bash
git diff --staged <commit_id_1> <commit_id_2> -- <file_name>
```

To see the changes in a specific file between two commits in the working directory, run the command:

```bash
git diff <commit_id_1> <commit_id_2> -- <file_name>
```

To see the changes in a specific file between two branches, run the command:

```bash
git diff <branch_name_1> <branch_name_2> -- <file_name>
```

To see the changes in a specific file between two tags, run the command:

```bash
git diff <tag_name_1> <tag_name_2> -- <file_name>
```

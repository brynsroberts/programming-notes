`git revert` is a Git command that creates a new commit that undoes the changes made by a previous commit. This is useful when you need to undo the changes made by a commit without removing it from the Git history. ([[reset]] changes the history)

When you run `git revert <commit>`, Git creates a new commit that contains the inverse changes of the specified commit. This new commit has a commit message that starts with "Revert" followed by the original commit message. The new commit has a different SHA-1 hash from the original commit, and it appears in the Git history as a new commit that undoes the changes made by the original commit.

For example, suppose you have the following Git history:

```
A -> B -> C -> D
```

If you want to revert the changes made by commit `C`, you can run `git revert C`. Git will create a new commit that undoes the changes made by commit `C`, and the Git history will look like this:

```
`A -> B -> C -> D -> E`
```

Where commit `E` is the new commit created by `git revert`.

Note that `git revert` does not remove the original commit from the Git history, and it does not modify any of the commits that came after the original commit. This means that you can use `git revert` to undo changes without affecting the work of other people who have already based their work on the original commit.
# Change history

If you (for some reason) need to change your email in git history, you can do the follow command:

```console
git filter-branch --commit-filter '
    if [ "$GIT_COMMITTER_EMAIL" = "new@email.com" ];
    then
            GIT_COMMITTER_EMAIL="new@email.com";
            GIT_AUTHOR_EMAIL="new@email.com";
            git commit-tree "$@";
    else
            git commit-tree "$@";
    fi' HEAD
```

_To change nickname, just change `GIT_COMMITTER_EMAIL` to `GIT_COMMITTER_NAME`_
# Clean outdates branches

### Local branches

_TBA_

---

### Remote branches

List of references remote branches

```console
$ git branch -r
```

Clean-up outdated branches

```console
$ git remote prune origin
```

_also you can update respository with the command below, and git automatically prunes all stale references_

```console
$ git fetch -p
```

---
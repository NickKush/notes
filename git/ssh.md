# SSH setup

---

### Generate new ssh key

```console
ssh-keygen -t ed25519 -f ~/.ssh/github
```

### Add key in ssh-agent
```console
eval $(ssh-agent -s)
ssh-add ~/.ssh/github
```

### Save settings in config file

File location - `~/.ssh/config`

```console
# Github
Host github.com
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/github
```


### Add public key to your github account

```console
cat ~/.ssh/github
```

Copy public key and add it in settings `https://github.com/settings/keys`


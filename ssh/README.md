# SSH

---

### Generate ssh key

```console
ssh-keygen -t rsa -f ~/.ssh/new_key
```

> `-t` type of key to create `dsa | ecdsa | ecdsa-sk | ed25519 | ed25519-sk | rsa`

> `-f` file to save


Add ssh key into ssh-agent

```console
eval $(ssh-agent -s) && ssh-add ~/.ssh/new_key
```

---

### Config file

Config file located in `~/.ssh/config`

Example for github

```
Host github.com
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/github
```

Example for vm

```
Host vm
  Hostname 192.168.0.10
  User user
  Port 22
```


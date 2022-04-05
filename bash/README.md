# Bash

You know what it is.

---

## Useful tips


### `^r`  

Reserve history for a command that was previously typed in the bash-history.

---

### `!!`

A substitution which contains the previous command.

```console
$ apt update
Reading package lists... Done
E: Could not open lock file /var/lib/apt/lists/lock - open (13: Permission denied)
E: Unable to lock directory /var/lib/apt/lists/

$ sudo !!
sudo apt update
[sudo] password for <username>:
Hit:1 ...
...
```

---

### `!$`

A substitution which contains the last segment of the previous command.

```console
$ $EDITOR main.py

$ python3 !$
python main.py
Hello bash!

$ echo !$
echo main.py
main.py
```

---

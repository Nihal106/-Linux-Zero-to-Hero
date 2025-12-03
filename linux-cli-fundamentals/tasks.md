# ✔ Task 1 – Navigation

* Go to /etc

* Hop to /var/log

* Go back to your home using one command

```bash
cd /etc
cd /var/log
cd ~
```

# ✔ Task 2 – File Search

### Find:
```bash
sshd_config
*.conf files in /etc
files larger than 5MB
directories inside /usr
```
```bash
find /etc -name sshd_config
find /etc -name "*.conf"
find / -type f -size +5M
find /usr -type d
```

# ✔ Task 3 – Wildcards

### Create:
```bash
touch file1.txt file2.txt fileA.log fileB.log
```

### Then:
```bash
ls file*.txt
ls file?.log
ls file[A-B].log
```

# ✔ Task 4 – Use pipe + grep
```bash
ps aux | grep ssh
ls /etc | grep conf
```

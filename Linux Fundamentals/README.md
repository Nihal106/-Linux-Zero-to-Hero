## 🔹 1. What is Linux?

Linux is an **open-source operating system** commonly used on servers, cloud, and development environments.

- **Kernel** — the core that manages CPU, memory, hardware  
- **Shell** — command-line interface (e.g., `bash`)  
- **File system** — hierarchical tree of files and folders  
- **Services & packages** — background software and system packages

---

## 🔹 2. What is RHEL (Red Hat Enterprise Linux)?

RHEL is an **enterprise-grade Linux distribution** used in production environments for stability, security, and long-term support.

> Alternatives with very similar behavior: Rocky Linux, AlmaLinux, CentOS Stream.

---

## 🔹 3. Setting Up Your Linux Environment


### AWS EC2
- Launch a small instance (free-tier: t2.micro / t3.micro) with Amazon Linux or RHEL.
- SSH example:
```bash
ssh -i yourkey.pem ec2-user@PUBLIC_IP
```

## 🔹 4. Linux Directory Structure (very important)

Run:
```bash
ls /
```

Common directories:

/bin — basic user commands (ls, cp, mv)

/sbin — system binaries (fdisk, shutdown)

/etc — system configuration files

/home — home folders for regular users

/root — root user's home

/var — variable data, logs

/usr — installed applications & libraries

/dev — device files

/proc — runtime system info (virtual filesystem)

/tmp — temporary files

Everything starts from / (root). Think of directories as a tree.

## 🔹 5. Your First Linux Commands
### Navigation
```bash
pwd        # show current directory
cd /etc    # go to /etc
cd ~       # go to home
cd -       # previous directory
ls         # list files
ls -l      # long listing
```

## Create files & folders
```bash
mkdir myfolder
touch file1.txt
echo "Hello Linux" > file2.txt
```


## Copy / Move / Delete
```bash
cp file1.txt backup.txt
mv file1.txt /tmp/
rm file2.txt
rm -r myfolder
```

## 🔹 6. Getting Help
```bash
man ls       # full manual for `ls`
ls --help    # quick help
history      # list previous commands
# Press `q` to exit `man`
```

## 🔹 7. Practice Tasks 
### Task 1 — Navigate Linux
```bash
cd /etc
cd /var/log
cd ~      # return to your home directory
```

## Task 2 — File operations
```bash
mkdir ~/day1
cd ~/day1
touch a.txt b.txt c.txt
cp a.txt /tmp/
rm c.txt
mv ~/day1 /home/<yourname>/practice
```

## Replace <yourname> with your actual username.

## Task 3 — Explore system info
```bash
ls /
whoami
hostnamectl
uname -r
uptime
```

# Linux CLI Fundamentals

# 🔹 1. Absolute vs Relative Paths

A path tells Linux where a file or a directory is located.

## ✔ Absolute Path
- Starts from the **root directory `/`**
- Always the full path
- Works from anywhere

### Examples:
```bash
cd /var/log
cd /home/user/day1
cd /usr/share/doc
```
## ✔ Relative Path

- Based on current directory

- Shorthand navigation

- Uses **. , .. ,  ~ , -**

### Symbols:
  | Symbol | Meaning            |
  | ------ | ------------------ |
  | `.`    | Current directory  |
  | `..`   | Parent directory   |
  | `~`    | Home directory     |
  | `-`    | Previous directory |


### Examples:

```bash
cd ../              # go one directory up
cd ./scripts        # go to 'scripts' in current folder
cd ../../etc        # go up 2 levels then to /etc
```

Try this:
```bash
cd /etc
cd ../var/log
```
# 🔹 2. Important Navigation Commands
## ✔ Show current directory:
  ```bash
    pwd
  ```

## ✔ List files:
  ```bash
ls           # normal list
ls -l        # long list (permissions, owner, time)
ls -a        # show hidden files (like .bashrc)
ls -lh       # long list + human readable size
  ```
✔ Change directories:
  ```bash
  cd /etc      # go to /etc
  cd ~         # go to home directory
  cd -         # jump to previous directory
  cd ..        # go to parent directory
  ```
# 🔹 3. Useful Bash Shortcuts (VERY IMPORTANT)
  | Shortcut     | Meaning              |
  | ------------ | -------------------- |
  | **Tab**      | Auto-complete        |
  | **↑ ↓**      | Command history      |
  | **Ctrl + C** | Stop running command |
  | **Ctrl + L** | Clear screen         |
  | **Ctrl + A** | Go to start of line  |
  | **Ctrl + E** | Go to end of line    |
  | **Ctrl + U** | Clear entire line    |
  | **Ctrl + R** | Search history       |


### Example:
Press **Ctrl + R**, type **ssh**, and it shows your last SSH command.

# 🔹 4. Wildcards (Globbing)

  Used to match multiple files using patterns.

## ⭐ Asterisk *

  Matches zero or more characters.
  ```bash
  ls *.txt           # all txt files
  rm file*           # files starting with 'file'
  ls log*2024.log    # logs that start with log...2024.log
  ```
## ⭐ Question Mark ?

  Matches one character.
  ```bash
  ls file?.txt       # file1.txt, fileA.txt but NOT file10.txt
  ```
## ⭐ Square Brackets []

  Matches range or set of characters.
  ```bash
ls file[0-9].txt   # file1.txt, file9.txt
ls file[a-c].log   # filea.log, fileb.log, filec.log
  ```

# 🔹 5. Display File Content
  ```bash
cat filename         # print file to screen
less filename        # scroll through file
head -n 10 file      # first 10 lines
tail -n 20 file      # last 20 lines
tail -f file         # real-time logs (very useful)
  ```
### tail -f is commonly used for watching logs live:
```bash
tail -f /var/log/messages
```
# 🔹 6. File Searching (VERY IMPORTANT)
## ⭐ find — live search
  ```bash
  find /etc -name sshd_config
  find /var -type f -size +10M
  find . -type d
  ```
## ⭐ locate — fast search

### Install database (RHEL-based systems):
  ```bash
  sudo dnf install mlocate
  sudo updatedb
  ```

### Use locate:
  ```bash
  locate sshd_config
  locate *.conf
  ```
# 🔹 7. Command History (VERY USEFUL)
  ```bash
history             # show previous commands
!!                  # repeat last command
!45                 # run command number 45
!ls                 # run last ls command
  ```
# 🔹 8. Redirection & Piping
## ✔ Output redirection
  ```bash
ls > output.txt      # overwrite file
ls >> output.txt     # append to file
  ```
## ✔ Error redirection
  ```bash
  command 2> error.txt
  ```
## ✔ Piping
```bash
  ls | grep txt
  ps aux | grep ssh
```

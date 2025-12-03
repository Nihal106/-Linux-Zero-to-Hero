## 📄 File & Directory Creation
```bash
mkdir myfolder
touch file1.txt
echo "Hello Linux" > file2.txt
```
## 🧹 Move, Copy, Delete
```bash
cp file1.txt backup.txt
mv file1.txt /tmp/
rm file2.txt
rm -r myfolder
```
## 🔹 Getting Help in Linux

### Always remember these:
```bash
man ls            → manual for ls
ls --help         → quick help
history           → previous commands
``` 

Use q to exit man pages.


## ✔ Task 1: Navigate Linux

* Go to /etc
  ```bash
  cd /etc
  ```
* Go to /var/log
   ```bash
  cd /var/log
  ```
* Return to home using one command
    ```bash
  cd ~

  ```

## ✔ Task 2: File Operations

* Create folder day1
  ```bash
  mkdir ~/day1
  ```
* Inside it, create 3 files
  ```bash
  cd ~/day1
  touch a.txt b.txt c.txt
  ```
* Copy 1 file to /tmp
  ```bash
  cp a.txt /tmp/
  ```
* Delete one file
  ```bash
  rm c.txt
  ```
* Move folder to /home/<yourname>/practice
  ```bash
  mv ~/day1 /home/<yourname>/practice 
  ```

## ✔ Task 3: Explore System

* Run:
  ```bash
  ls /  # List Root Directory
  whoami # Show Current Logged-In User
  hostnamectl # System Hostname & OS Details
  uname -r # Show Kernel Version
  uptime # Show System Uptime
  ```

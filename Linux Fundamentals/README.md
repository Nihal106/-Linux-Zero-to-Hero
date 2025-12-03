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

* /bin — it contains basic user command (ls, cp, mv) binary files.

* /sbin — system binaries (fdisk, shutdown)

* /etc — all system configuration files are stored in the /etc.

* /home — this directory is where user folders are located. These includes Desktop, Documents, Downloads, Music, Videos etc.

* /root — this directory is the home directory of the root users.

* /var — this directory contains log files of various system applications.

* /usr — applications and user utilities are found in the /usr directory.

* /dev — it contains devices files such as /dev/sda. eg: it is storing the details of permenant storage like harddrives.

* /proc — this directory is a virtual file system that holds information on currently running processes. its a strange file system that is created upon system boot and destroyed upon shutdown.

* /tmp — temporary files

* /boot — static boot files are located in the /boot.

* /opt — for addon application package check them out in the /opt.

* /media — it stores files for removable devices such as USB drivers.

* /mnt — it contains sub directories that act as temperory mount points for mounting devices such as CD-ROMS.

* /lib — this directory stores shared library images and kernel modules.

Everything starts from / (root). Think of directories as a tree.

## 🔹 5. Your First Linux Commands
### Navigation
```bash
sudo su    # 'super user do switch user' To change the user to root user(to get all permissions)
pwd        # show current directory
cd /etc    # go to /etc
cd ~       # go to home
cd -       # previous directory
ls         # list files
ls -l      # long listing
ls -a      # list of all files and folders including hidden
ls -la     # long listing of all files and folders including hidden
```
---

# 🐧 Popular Linux Distributions (Fully Explained)

Linux comes in many variants called **distributions**.  
Each distribution has different purposes such as enterprise servers, development, cloud, and security.

Below are the most important ones you should know:

---

## 🔹 Enterprise / Server Linux Distributions

These are mainly used by companies, data centers, and production servers.

### **1. RHEL (Red Hat Enterprise Linux)**
- Most widely used Linux in the industry  
- Extremely stable  
- Comes with enterprise support  
- Basis for RHCSA, RHCE certifications  

### **2. Rocky Linux**
- Free version of RHEL  
- 100% bug-for-bug compatible  
- Created after CentOS shifted to CentOS Stream  

### **3. AlmaLinux**
- Another free RHEL-compatible Linux  
- Developed by community  
- Often used when migrating from CentOS  

### **4. CentOS Stream**
- Upstream of RHEL (rolling release)  
- Receives updates earlier than RHEL  
- Replaced the old CentOS project  

### **5. SUSE Linux Enterprise**
- Popular in Europe  
- Widely used in enterprise production servers  
- Known for stability and strong security  

### **6. Oracle Linux**
- Oracle’s version of RHEL  
- Used in Oracle Cloud & database environments  
- Free to use, paid support available  

---

## 🔹 Developer / Desktop Linux Distributions

Good for beginners, developers, and desktop usage.

### **1. Ubuntu**
- Most popular Linux distribution  
- Perfect for software development  
- Huge community support  
- Used widely in cloud and DevOps  

### **2. Debian**
- Very stable and secure  
- Base for Ubuntu  
- Preferred for servers that require long-term stability  

### **3. Fedora**
- Cutting-edge distribution backed by Red Hat  
- Gets the latest features first  
- Used by developers and enthusiasts  

### **4. Linux Mint**
- Beginner-friendly desktop Linux  
- Based on Ubuntu  
- Great UI, good for switching from Windows  

---

## 🔹 Cloud-Optimized Linux Distributions

Designed specifically for cloud platforms.

### **1. Amazon Linux 2023**
- Optimized for AWS  
- Fast, secure, lightweight  
- Ideal for EC2 instances  

### **2. Google Container-Optimized OS**
- Built for running containers  
- Used in Google Kubernetes Engine (GKE)  
- Very lightweight and secure  

### **3. Azure Linux**
- Microsoft’s cloud-optimized Linux  
- Used in Azure Kubernetes Service (AKS)  

---

## 🔹 Security & Special Purpose Linux

### **1. Kali Linux**
- Designed for penetration testing  
- Contains hundreds of security tools  

### **2. Parrot OS**
- Security, forensics, and hacking distribution  
- Lightweight alternative to Kali  

### **3. Arch Linux**
- Rolling release  
- Fully customizable  
- For advanced Linux users  

---

# 🔰 Summary of Distributions
- Enterprise servers → **RHEL, Rocky, AlmaLinux, SUSE, Oracle Linux**  
- Development & Desktop → **Ubuntu, Debian, Fedora, Mint**  
- Cloud environments → **Amazon Linux, Google COS, Azure Linux**  
- Security tools → **Kali, Parrot OS, Arch**  



# 🐧 Linux Basic Commands & Server Management Guide

![Linux](https://img.shields.io/badge/Linux-Terminal-black?logo=linux)
![Apache](https://img.shields.io/badge/Apache-WebServer-D22128?logo=apache)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?logo=mysql&logoColor=white)
![Status](https://img.shields.io/badge/Guide-ProductionReady-brightgreen)

---

# 📌 1️⃣ Basic Linux Commands

## 📂 File & Directory Commands

```bash
pwd                     # Show current directory
ls                      # List files
ls -al                  # List all files with details
cd foldername           # Change directory
cd ..                   # Go back one folder
mkdir foldername        # Create folder
rm filename             # Remove file
rm -rf foldername       # Remove folder
cp file1 file2          # Copy file
mv file1 file2          # Move/Rename file
```

---

## 📄 File Viewing & Editing

```bash
cat filename            # View file content
less filename           # Scroll view
nano filename           # Edit file
vi filename             # Edit file (advanced)
```

---

## 🔎 Search & Find

```bash
find / -name filename
grep "word" filename
```

---

# 🔐 2️⃣ User & Permission Commands

```bash
whoami                  # Current user
sudo su                 # Switch to root
chmod 755 filename      # Change permission
chown user:user file    # Change ownership
```

Permission format:
```
7 = read + write + execute
6 = read + write
5 = read + execute
```

---

# 🌐 3️⃣ Service Management (systemctl)

Check service status:
```bash
sudo systemctl status servicename
```

Start service:
```bash
sudo systemctl start servicename
```

Stop service:
```bash
sudo systemctl stop servicename
```

Restart service:
```bash
sudo systemctl restart servicename
```

Enable service on boot:
```bash
sudo systemctl enable servicename
```

---

# 🌍 4️⃣ Apache (Web Server)

## Start Apache

Ubuntu/Debian:
```bash
sudo systemctl start apache2
```

CentOS/RHEL:
```bash
sudo systemctl start httpd
```

## Restart Apache
```bash
sudo systemctl restart apache2
```

## Check Status
```bash
sudo systemctl status apache2
```

## Test Configuration
```bash
sudo apachectl configtest
```

Apache config location (Ubuntu):
```
/etc/apache2/
```

Website root:
```
/var/www/html/
```

---

# 🗄 5️⃣ MySQL / MariaDB

## Start MySQL

Ubuntu:
```bash
sudo systemctl start mysql
```

CentOS:
```bash
sudo systemctl start mysqld
```

## Restart MySQL
```bash
sudo systemctl restart mysql
```

## Check Status
```bash
sudo systemctl status mysql
```

## Login to MySQL
```bash
mysql -u root -p
```

---

# 🔄 6️⃣ Update Linux System

## Ubuntu / Debian

Update package list:
```bash
sudo apt update
```

Upgrade packages:
```bash
sudo apt upgrade -y
```

Full upgrade:
```bash
sudo apt full-upgrade -y
```

Clean unused packages:
```bash
sudo apt autoremove -y
```

---

## CentOS / RHEL

```bash
sudo yum update -y
```

or (newer systems)
```bash
sudo dnf update -y
```

---

# 🌐 7️⃣ Network Commands

```bash
ip a                    # Show IP address
ping google.com         # Test connectivity
netstat -tulpn          # Show open ports
ss -tulpn               # Modern alternative
```

---

# 💾 8️⃣ Disk & Memory

```bash
df -h                   # Disk usage
du -sh foldername       # Folder size
free -m                 # Memory usage
top                     # Process monitor
htop                    # Advanced monitor
```

---

# 📦 9️⃣ Install Common Packages (Ubuntu)

```bash
sudo apt install apache2
sudo apt install mysql-server
sudo apt install php
```

---

# 🚀 1️⃣0️⃣ Basic LAMP Stack Install (Ubuntu)

```bash
sudo apt update
sudo apt install apache2 mysql-server php libapache2-mod-php php-mysql
```

---

# 🔥 Production Tips

✔ Always update system regularly  
✔ Always test config before restart  
✔ Enable firewall (ufw)  
✔ Disable root SSH login  
✔ Backup before major updates  

---

# 🧠 Quick Cheat Sheet

```bash
sudo systemctl restart apache2
sudo systemctl restart mysql
sudo apt update && sudo apt upgrade -y
ip a
df -h
top
```

---

🚀 Maintained by: Vigneshwaran R

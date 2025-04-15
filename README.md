# Tools Prerequisites

Panduan instalasi tools umum untuk **Ubuntu 24.04** dan **CentOS 9 / RHEL9 / Rocky Linux**.

---

## 🐧 Ubuntu 24.04

### 1. Install VirtualBox

```
sudo apt update
```

```
sudo apt install curl wget gnupg2 lsb-release -y
```

```
curl -fsSL https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/vbox.gpg
```

```
curl -fsSL https://www.virtualbox.org/download/oracle_vbox.asc | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/oracle_vbox.gpg
```

```
echo "deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian $(lsb_release -sc) contrib" | sudo tee /etc/apt/sources.list.d/virtualbox.list
```

```
sudo apt update
```

```
sudo apt install -y linux-headers-$(uname -r) dkms
```

```
sudo apt install virtualbox-7.1 -y
```

```
sudo usermod -aG vboxusers $USER
```

```
newgrp vboxusers
```

### 2. Install Vagrant

```
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
````

```
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
````

```
sudo apt update
````
```
sudo apt install vagrant
```
```
libarchive-dev libarchive-tools -y
```

### 3. Install Git

```
sudo apt install git -y
```

---

### 4. Install JDK 17

```
sudo apt-get install openjdk-17-jdk -y
```

---

### 5. Install Maven

```
sudo apt-get install maven -y
```

---

### 6. Install VSCode

```
sudo apt-get install wget gpg -y
```

```
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
```

```
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
```

```
echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" | sudo tee /etc/apt/sources.list.d/vscode.list > /dev/null
```

```
rm -f packages.microsoft.gpg
```

```
sudo apt install apt-transport-https -y
```

```
sudo apt update
```

```
sudo apt install code -y
```

---

### 7. Install Sublime Text

```
sudo apt update
```

```
sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common -y
```

```
curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
```

```
sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"
```

```
sudo apt install sublime-text -y
```







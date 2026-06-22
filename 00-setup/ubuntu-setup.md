# Ubuntu linux operating system setup

## Goal

Prepare Ubuntu for learning linux, Bash scripting, Git, and command-line automation.  


---
### 1. Check system information

```bash
lsb_release -a
uname -a
whoami
pwd

```
### Notes

| Command        | Meaning                            |
|----------------|------------------------------------|
|`lsb_release -a`| shows ubuntu version info          |
|`uname -a`      | shows kernel and syst info         |
|`whoami`        | shows the current logged-in user   |
|`pwd`           | shows the current working directory|

---


### 2. Update package lists

```bash
sudo apt update

```
#### 
This refreshers Ubuntu's list of available packages from configured repositories.

---


### 3. Upgrade installed packages

```bash
sudo apt upgrade -y

```

### Meaning 
This upgrades installed packages to newer available versions.

----


----
### 4. Install essential tools

```bash
sudo apt install -y build-essential curl wget git tree unzip zip nano vim htop

```

### Tools installed

| Tool             | Purpose                          | 
| -----------------| ---------------------------------|
|`build-essential` | Compiler and build tools         |
|`curl`            | Fetch data from URLs             |
|`wget`            | Download files                   |
|`tree`            | View folder stractures           |
|`git`             | Version control                  |
|`unzip`           | Extract `.zip` files             |
|`zip`             | Create `.zip` files              |
|`nano`            | Beginner-friendly terminal editor|
|`vim`             | Advanced terminal editor         |
|`htop`            | Interactive process viewer       |

---

### 5. Check installed versions

```bash
bash --version
git --version
curl --version
wget --version
tree --version

```

---

### 6. Confirm default shell

```bash
echo $SHELL

```
Expected commo output:  
```text
/bin/bash

```

If it shows something else, that is not automatically bad. It only tells us your default login shell.  


---

### 7. Create a safe practice folder
```bash
mkdir -p ~/linux-pracice
cd ~/linux-practice
mkdir files scripts logs backups temp
tree

```

---

### 8. Setup completed checklist
- [] Checked Ubuntu version. 
- [] Updated package lists. 
- [] Upgraded packages. 
- [] Installed essential tools.
- [] Checked Bash version. 
- [] Checked Git version. 
- [] Confirmed my shell.  
- [] Created `~/linux-practice`.

---


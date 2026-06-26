# 1. Bash Basics
## Introduction
Bash (Bourne Again Shell) is acommand-line interpreter commonly used in Linux and Unix-based operating systems. It allowa users to interactwith the operating system by typing commands instead of using a graphical interface. Bash provides a fast and efficient way to:  
navigate directories,  
manage files,  
automate taks,  
and administer systems.  

Learning basic Bash commands is an essential skill for linux users, system administsrators, software developers and cybersecurity professionals. Understanding commands such as `ls`, `cd`, `pwd`, and `mkdir` help users navigate the file system, inspect directory conteents and work more effecively in aterminal environment. This guide introduces fundamental Bsh commands and their commonly used options.  

---
## 1. The `ls` Command
### i. Purpose
- List files and directories.
- Helps inspet folder contents.
- Can display hidden files and permissions.

### ii. Basic Syntax

---
| Command | Description/ Function | Example |
|-------------|---------------------| ------|
| `-l` | Long listing | `ls -l` |
| `-a` | Show hidden files | `ls -a`|
| `-h` | Human-readable sizes | `ls -h` |
| `-t` | Sort by modification time | `ls -t` |
| `-r` | Reverse Sorting | `ls -r` | 
| `-R` | List subdirectories recursively | `ls -R`|
| `-S` | Sort by file size | `ls -S` |
| `-1` | one file per line | `ls -1` | 
| `-d` | list directories themselves not their token | `ls -d` |
| `-F` | Append file indicators | `ls -F` | 
| `--color=auto` | Colorized ooutput | `ls --color=auto` |

---
### iii. Combining Options
```bash
ls -lah
```
[] Breakdown
- l => long listing
- a => list including hidden files
- h => human-readable sizes

### iv. Understanding Hidden Files
- Hidden files start with `.`
- Examples:
        - `.baashrc`
        - `.gitignore`
        - `.profile`
- Command example:
 ```bash
 ls -a
 ```
 ---
 ## 2.Directory Navigation `cd`
 ### i. Purpose
 - it is used to change/ navigate through directories
 ### ii. Common Commands

 | Command | Meaning |
 |------| ------- |
 | `cd` | Go to home directory |
 | `cd ~` | Go to home directory | 
 | `cd ..` | Move one level up |
 | `cd - ` | switch to previous directory| 
 | `cd / ` | Change to Root Directory | 
 | `cd foldername` | Enter a folder |

 ---

 ## 3. The `pwd` command
 ### i. Purpose
 - it shows hte current working directory.

 | Command | Meaning |
 |-----------|---------|
 | `pwd -l` | Displays the logical current working directory. |
 | `pwd -P` | Displays the physical current working directory.|
 
 ---

 ## 4. The `echo ` command
 ### i. Purpose
 - Used to show a line of text or variables in the terminal.

 | Command | Meaning |
 |----------|----------|
 | `echo -n` | Dont add  a  new line at the end |
 | `echo -e` | Allows special  characters ie. `\n` for new lines |
 | `echo -E` | Don't  allow special characters (Default)|

 ---

 ## 5. The `cat` Command
 ### i. Purpose
 - Used to show the contents of a file in a terminal.
 - It can also be used to combine multile files

 ### ii. Basic usage
 ```bash
 cat filename
 ```
 | Command | Meaning |
 |---------|-------------|
 | `cat -n` | Add numbers to each line |
 | `cat -b` | Add numbers only to lines with text |
 | `cat -s` | Remove extra lines |
 | `cat -v` | Show non-printing characters(Except for tabs and end of lines) |

 ---

 ## 6. The `cp` Command
 ### i. Purpose
 - Used to copy  files and directories from one location to another.
 ### ii. Basic usage
 ```bash
 cp source_file destination_file
 ```
 | Command | Meaning |
 |-------------|---------|
 | `cp -r` | Copy all files and folders in a directory |
 | `cp -i` | Ask  before replacing files |
 | `cp -u` | Copyonly if the source is newer |
 | `cp -v` | Verbose mode, show files being copied|

 ---

 ### iii. `cp` with  wildcards
 ```bash
 cp *.txt /destination/
 ```
 - it is used to copymultiple files.

 ## 7.The `mv` command
 ### i. Purpose
 - It is used to move files and directories
 - It is  also used to rename files and directories.
 ### ii. Basic usage
 ```bash
 mv source_file destination_file
 ```
 or 
 ```bash
 mv old_filename new-filename
 ```
 when renaming a file or directory
 ---
 | Command | Meaning |
 |----------|-----------|
 | `mv -i` | Ask before replacing |
 | `mv -u` | Move only if the source is newer |
 | `mv -v` | Verbose mode, Show files or directories being moved |

 ### iii. `mv` with wildcards
 ```bash
 mv *.txt /destination/
 ```
 - it used to move multiple files.

## 8. The `rm` Command
### i. Purpose
- Used to remove files or directtories
### ii. Basic  usage
```bash
rm filename
```

| Command | Meaning | 
|-----------|--------|
| `rm -r` | Delete a folser and everything inside it. |
| `rm -i` | Ask before deleting files |
| `rm -f` | Force deleting without asking |
| `rm -v` | Verbose mode,  Show  the files/foldersbeing deleted|

---

```bash
rm *.class 
```
- This Deletes all the files with a .class extension inside the current directory.

## The `touch` Command
### i.  Purpose
- Used to change the time stamps or create an empty file if it does not exist.

### ii. Basic usage
```bash
touch filename
```
| Command | Meaning |
|-----------|---------|
| `touch -a` | update only when the file was last used |
| `touch -m` | Update only when the file was last changed |
| `touch -t` | Set the timestamp to a specific time `touch -t 202601010000 test.txt` |
| `touch -c` | Do not create any files |

---

## 9. The `mkdir` Command
### i.Purpose
- Used to create new directories 

```bash
mkdir folder_name
```
| Command | Meaning |
|-----------|-----------|
| `mkdir -p` | Parent direcories as needed |
| `mkdir -v` | Show a message for each created directory |
| `mkdir -m` | set file  permission ```bash  mkdir -m 755 ``` |

![File Permissions](permission.png)

---

## 10. The `man`  Command
### i.Purpose
- Used to display the user manual of any command that can be run on terminal

```bash
man command_name
```
[] ie. `man ls`

---
## 11. Bash `alias`
### i. Purpose
- it allows a user to create a shortcut for a long or frequently used command
- This makes it easy to execute complex commands with a simple keyword

```bash
alias name='command'
```
[] name is the shortcut name you want to use.  
[] command is the full command you want to execute

----
-for removing an alias:
```bash
unalias name
```
---------------------------------------------------------------------------

# 2. Text Processing in Linux:
## Goal
Learn how to search, modify, and analyze text files using linux commands

## 1. The `grep` Command
### i. Purpose
The `grep` command searches for lines that contain a specific word, pattern or expression.
### ii. Basic syntax.
```bash
grep pattern filename
```
- example: `grep John students.txt
- The output should be any occurence of the word John in the file students.txt

| Command | Meaning | Examples|
|-----------|----------|---------|
| `grep -i` | Search ignoring the case difference| `grep -i John students.txt` |
| `grep -r` | Search through all files in a directory and its subdirectories | `grep -r John .` |
| `grep -v` | Find lines that do not match the pattern | `grep -v John students.txt` |
| `grep -n` | Show line numbers | `grep -n John students.txt` |

---

## 2. The `awk` Command
###  i. Purpose
- This commmand is used for pattern scanning and processing language.
- Useful for handling text files and is used for data extraction and reporting

```bash
awk 'pattern {action}' filename
```
Example:
```bash
awk -F "," '*{print $1}' filename
```
- `awk -F` => set what separates the data fields.
- `awk -v` => set variables to be used in the script.
- `awk -f` => Use a file as the source of the awk program.

---

## 4. The `sed` Command
### i. Purpose
- It is a stream editor used to perform basic text transformations on an input stream( a file or input from a pipeline).
- it is used to replace a text or word in a file.
 ```bash
 sed 's/old_text/new_text/g' filename
 ```
 | Command | Meaning |
 |------|-------|
 | `sed -i` | Edit files directly without needing to save the file  separately|
 | `sed -e` | Add the script to the commands to be executed |
 | `sed -n` | Don't automatically print lines |
 | `sed -r` | use extended regular expression |
 | `sed -f` | Add script from a file |
 | `sed -l` | specify line leength fo `l` command |
 | `sed -n` | print  or delete a specific line |

 ----

 ## 5. The`cut` Command
### i. Purpose
- It is used to remove sections from each line of files.
- It is useful for extracting specific tools of data froma file or output stream.

| command | Meaning |
|---------|---------|
| `cut -d` | Choose what separates the field ie: `cut -d "," -f1 exapmle.txt` |
| `cut -f` | Select specific fields to display  ie: `cu -f1 example.txt`  means that it will display the first culumn of the data|
| `cut --complement` | Show all the field except the selected ones |

---

## 6. The `sort` Command
### purpose
- Used to sort lines of text
```bash
sort filename
```
| Command | Meaning |
|---------| ------|
| `sort -r` | Sort the data in reveerse order |
| `sort -n` | Sort numbers correctly |
| `sort -k` | Sort by specific column |
| `sort -u` | Remove duplicates |
| `sort -t` | Specify a delimeter for fields |

---

## 7. The `tail` command
(view end)
- It is used to display the last part of a file
```bash
tail-n lines file_name
```
| Command | Meaning |
|-----|------|
| `tail -n [number]` | Displays the last [number] line of a file |
| `tail -f` | Follow the file as it grows |
| `tail -c [number]` | Display the last [number] bytes of a file|
| `tail --pid=[pid]` | Terminate after the process with the given pid dies |
| `tail --retry` | Keep tring to open a fileeven if its inaccesible |

Example:
```bash
tail -n 5 logfile.txt
```
The `tail` command is useful for;
- Monitoring server logs and detecting errors in real time.
- Checking the latest entries in a continuously updated file.
- Debugging applications by reviewing recent log files.

---

## 8. The `head` command
(view start)
- Displays The first part of a  file 
```bash
head file_name
````
- [] `head -n [number] ` => Displays the first [number]lines of a file.
- [] `head -c [number]` => Displays the first [number] bytes of a file.

- For multiple files :
```bash
head -n 5 file1 file2 file3--
```

```bash
head -q
``` 
This command suppresses printing of headers when multiple files are being printed.

---


# 3. SYSTEM MONITORING
## 1. The `ps` Command









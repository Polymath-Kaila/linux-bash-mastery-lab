## GOAL
Understand:  
1. filesystem
2. paths
3. files
4. permissions
5. users
6. commands
7. processes

Main quiz:  

What is the system state, and how do I inspect or change it safely?

## TRICKS IN COMMANDS

### 2.echo
1. Prinot with colors ``` echo -e "\033[031mRed text\[0m" ```
2. Show all files in a var ``` echo *, echo *.txt, echo{1,...10}```

#### 2.touch
1. create multiple files at once ``` touch {a,b,c...}.txt ```
2. change timestamps ```touch -t yymmddtt file.txt``` or ```bash touch -r changethistimestamp.txt tothistimestamp.txt```
3. create files with specific timestamps ```touch -d "2 days ago" old.txt ``` or ``` touch -d "2025-12-25 12:00" xmas.txt```

### 3. ls
1. show subdirectories with directories ```ls -lR ```
2. long listing with inode numbers ```ls -li```
3. show only directories ```ls -l | grep ^d ```

### 4. mkdir
1. creating nested directories at once ```mkdir -p project/src/images```
2. creating multiple directories in a go ```mkdir {dir1...dir5}```
```bash
mkdir -p projects/{src,bin,docs} 
# creates nested structure
```
3. creating with permissions
```bash
mkdir -m 700 secret-folder  # only YOU can access it
mkdir -m 755 public-folder # Everyone can read, only i can write
```
4. Verbose
```bash
mkdir -v new_folder
```
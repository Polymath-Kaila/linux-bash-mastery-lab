# Command Anatomy

Most linux commands follow certain anatomy:  

` command options arguments `.  

```bash
ls -lah /etc

```

|-|-|-|
|command| ls | the action|
|options| -lah| modifies how `ls` behaves|
|argument| /etc| the target `ls` works on |


### Copy command in depth

```bash
cp -r notes backup

```

|part| value| meaning|
|-|-|-|
|command| cp | copy|
|option| -r | copy recursively|
|argument 1|notes|source|
|argument 2|backup|destination|

---

A command can be several things, it can be a shell builtin, a shell function, an alias, or an external executable.   


`Principle`: A command name is a name that the shell must resolve.  

---

## The 5 command types

### 1. Alias
An alias is a shortcut. It is text replacement done by shell.  

Example:  
```bash
alias ll='ls -lah'

```

So When we type, ll the shell expands to `ls -lah`.  
An alias is not a real program file.  
---
### 2. Shell function
A function is small named block of shell logic.  

Example:  
```bash
mkdc(){
    mkdir -p "$1"
    cd "$1"
}
```
Then:  

```bash
mkdc test

```
Means:   
make directory test, then enter the directory test.  

---

### 3. Shell builtin
A builtin is a command built into the shell itself.  

Example:  


```bash
cd
ls
echo
type
alias
help
```

---

### 4. External executable
This is real program file stored somewhere in the filesystem.  

Examples:   
```bash
/bin/ls
/urs/bin/grep
/usr/bin/find
```
Executable = real file on disk that the OS can run as a process.  

---

### 5. Missing command

If shell cannot resolve the first word, we get command not found.  


---
#### Summay:

The shell does not simply run words.
The shell resolves names.

A command line has:
- a command name
- options
- arguments

The command name may resolve to:
- alias
- function
- builtin
- executable
- nothing

If it resolves, the shell either handles it internally or runs a program.
If it fails, the error tells me where resolution or execution broke.
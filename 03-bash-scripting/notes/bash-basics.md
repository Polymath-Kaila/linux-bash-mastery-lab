# Intro to bash and shell

 `A terminal` is just the interface where we type the commands.  
 `Shell` is a command interpreter that lets us talk to the OS.  
 `Bash` is one of the popular shell used in linux.  
 `Bash command` is just the command or something you type in the terminal.  
 `Bash script` is just a file containing multiple bash commands.  
 

### Examples of terminals
+ vs code terminal
+ windows powershell
+ ubuntu terminal

 ### Examples of shells
 + sh
 + zhs
 + fish
 + bash

 ## Checking your type of shell
 ```bash
 echo $SHELL

 ```
 ## Checking your bash version
 ```bash
 bash --version

 ```

 ### Examples of bash commands
 A bash comma
 ```bash
 ls 
 cd Desktop
 ```
### Example of a bash script
```bash
#!/usr/bin/env bash

echo "Starting backup..."
mkdir -p backups
cp notes.txt backups/
echo "Backup complete."

```
`!#/usr/bin/env bash` - tells the shell system to run the script/file using bash.   


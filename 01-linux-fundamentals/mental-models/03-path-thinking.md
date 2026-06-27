# Path Thinking

## System reality

Linux stores files and directories inside one filesystem tree.

Every command that works with a file or directory must resolve a path into an actual filesystem object.

## First principle

A path is an address.

The shell and operating system must resolve that address before any action can happen.

## Mental model

I am always standing somewhere in the filesystem.

That location is called the current working directory.

Relative paths start from where I am standing.

Absolute paths start from root `/`.

## Path types

| Type | Example | Meaning |
|---|---|---|
| Absolute path | `/home/polymath/Desktop/file.txt` | Start from root |
| Relative path | `Desktop/file.txt` | Start from current directory |
| Current directory | `./script.sh` | File inside current directory |
| Parent directory | `../notes.txt` | File one level above |
| Home shortcut | `~/Desktop/file.txt` | File inside my home directory |

## Core rule

If a path starts with `/`, it is absolute.

If it does not start with `/`, it is relative.


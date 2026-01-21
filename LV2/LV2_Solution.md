# Bandit Level 1 → Level 2
<img width="732" height="328" alt="image" src="https://github.com/user-attachments/assets/e97efe2c-2319-494c-b9c4-65d5c27bce33" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit2**.

## Description
The challenge states that the password for the next level is stored in a file called `-`, which is located in the home directory.  
Because the filename starts with a dash (`-`), it cannot be accessed in the usual way, as the shell interprets it as an option.

## Methodology
First, the contents of the home directory are listed to confirm the presence of the file named `-`.  
To read this file, a special syntax must be used so that the dash is treated as a filename and not as a command option.

This can be done by explicitly specifying the path to the file.

<img width="1541" height="110" alt="image" src="https://github.com/user-attachments/assets/c4e43c01-9f7b-46a9-8f43-e67150f00434" />


## Commands Used
```bash
ls
cat ./-




# Bandit Level 2 → Level 3
<img width="878" height="305" alt="image" src="https://github.com/user-attachments/assets/9844be37-9f42-4935-bcfc-9c114eeffb99" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit3**.

## Description
The challenge states that the password for the next level is stored in a file called  
`--spaces in this filename--`, which is located in the home directory.

Because the filename contains spaces, it cannot be accessed directly without proper escaping or quoting.

## Methodology
First, the files in the home directory are listed to identify the file with spaces in its name.  
To read the file correctly, the filename must be wrapped in quotes so the shell interprets it as a single argument. 
Additionally, `--` is used to explicitly indicate the end of command options, ensuring the filename is not interpreted as an option.

<img width="1662" height="92" alt="image" src="https://github.com/user-attachments/assets/6141d6e5-4e02-454d-9ccc-e77dea76cd8c" />

## Commands Used
```bash
ls
cat -- "--spaces in this filename--"


